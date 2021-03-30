<template>
  <div id="app">
    <Header />
    <div class="content-wrapper">
    <div class="filter-section-wrapper">
        <FilterSection @refetch-data="refetchData" />
        <div class="date-picker-wrapper">
          <date-picker v-model="date" lang="en" range type='date' format="MMM-DD-YYYY"></date-picker>
          <input type="submit" value="Apply" @click="updateDate(date)" class="btn btn-block" />
        </div>
        </div>
        <Events :events="events" />
        <Footer />
    </div>
    
  </div>
</template>

<script>
import Header from './components/Header'
import Events from './components/Events'
import Footer from './components/Footer'
import FilterSection from './components/FilterSection'
import DatePicker from 'vue2-datepicker';
import 'vue2-datepicker/index.css';
import moment from 'moment'

export default {
  
  name: 'App',
  data() {
    return {
      events: [],
      date: null,
      ep: ''
    }
  },
  components: {
    Header,
    Events,
    FilterSection,
    DatePicker,
    Footer

  },
  methods: {
    async getData() {
      const res = await fetch('https://challenge.nfhsnetwork.com/v2/search/events/upcoming?state_association_key=18bad24aaa&amp;card=true&amp;size=50&amp;start=0')
      this.ep = res.url
      const data = await res.json()
     
      return data.items
    },
    async refetchData(id) {
      const res = await fetch(`https://challenge.nfhsnetwork.com/v2/search/events/upcoming?state_association_key=${id}&amp;card=true&amp;size=50&amp;start=0`)
      const data = await res.json()
      this.events = data.items
      this.ep = res.url
      return data.items
    },
    async updateDate(date) {
        var formattedDateStart = moment(date[0]).utc().format()
        var formattedDateEnd = moment(date[1]).utc().format()
        var apiString = `&from=${formattedDateStart}&to=${formattedDateEnd}`
        const res = await fetch(`${this.ep}${apiString}`)
        const data = await res.json()
        this.events = data.items
        return data.items
    }
      
  },
  async created() {
    this.events = await this.getData()
  }
}
</script>

<style>
#app {
background-color: #112;
width: 100%
}

.content-wrapper {
    width: 100%;
    background-color: #09121a;
    height: calc(90vh - 100px);
    padding-top: 40px;
}

body {
margin: 0;
background-color: #09121a;
}
.date-picker-wrapper {
  width: 90%;
  display: flex;
  justify-content: flex-end;
  font-family: 'Montserrat', sans-serif;
}

.mx-datepicker-main {
  background-color: #05243f;
  border: none;
  font-family: 'Montserrat', sans-serif;
}

.mx-calendar {
  color: #fff;
  font-family: 'Montserrat', sans-serif;
}

.logo  > img {
  position: relative;
  top: 20px;
  margin-left: 25px;
}

.mx-calendar+.mx-calendar {
    border-left: none;
    font-family: 'Montserrat', sans-serif;
}

.mx-btn-text {
    color: white;
    font-size: 24px;
    font-family: 'Montserrat', sans-serif;
}

.mx-calendar-header {
  justify-content: space-between;
  position: relative;
  height: 88px;
  display: flex;
  align-items: flex-end;
  font-family: 'Montserrat', sans-serif;
}

.mx-calendar-header-label {
  position: absolute;
  top:8px;
  left: 64px;
  font-family: 'Montserrat', sans-serif;
}

.btn-block {
  height: 44px;
  width: 90px;
  margin-left: 5px;
  border: 1px solid #00529b;
  background-color: transparent;
  color: white;
  font-family: 'Montserrat', sans-serif;
  border-radius: 4px;
  z-index: 100000;
  cursor: pointer;
}

.mx-input {
    display: inline-block;
    padding: 5px 0 7px;
    margin: 0;
    background-color: transparent;
    height: 42px;
    width: 100%;
    color: #fff;
    font-family: Montserrat,sans-serif;
    font-weight: 500;
    font-size: 16px;
    border-radius: 0;
    border: none;
    border-bottom: 1px solid #0e75d2;
    font-family: 'Montserrat', sans-serif;
}

@media (max-width: 1080px) {
  .nav {
    width: 100% !important;
    padding-left: 30px;
  }

  .date-picker-wrapper {
    width: calc(99% - 10px);
    padding-right: 30px;
  }

  #search {
    width: 142% !important;
  }

.nav-right {
  display: none;
}

.browse {
  display: none;
}

.search-wrapper {
  display: none;
}
}

@media (max-width: 800px) {

  #app {
    width: 103%;
  }
  .nav {
    top: -30px !important;
  }

  .nav > .menu-item {
    width: 93% !important;
  }

  .mx-datepicker-range {
      width: 84%;
  }

  .cards {
    width: 50% !important;
  }

  .footer-column {
    display: none;
  
}
.footer-popular {
    display: none !important;
  
}

}



@media (max-width: 800px) {

  .cards {
    width: 100% !important;
  }

  .cards-wrapper {
    margin-right: 0 !important;
  }

}
</style>
