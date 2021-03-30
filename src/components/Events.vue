<template>
  <div class="events-wrapper">
    <div class="table-wrapper">
      <table>
        <div class="row-wrap">
          <tr class="table-titles">
            <th>Key</th>
            <th>Headline</th>
            <th>SubHeadline</th>
            <th>Start Time</th>
          </tr>
        </div>
        <div class="cards-wrapper">
          <div v-for="event in events" :key="event.id" class="cards">
          <div class="row-wrap">
            <tr>
              <th class="event-key-col">{{ event.key }}</th>
              <th class="event-headline">{{ event.level }} {{ event.sport }}</th>
              <th class="subHeadline">
                <span class='probablyThere'>{{event.participants[0].short_name}}</span><span class='possiblyMissing' v-if="event.participants[1] !== undefined"> <span class="vs">vs</span> {{event.participants[1].short_name}}</span>
              </th>
              <th class="event-start-time">{{event.start_time | moment}}</th>
            </tr>
          </div>
        </div>

        </div>
      </table>
    </div>
  </div>
</template>


<script>
import moment from 'moment'
export default {
  name: "Events",
  props: {
      events: Array
  },
  filters: {
      moment: function(date) {
          return moment(date).format('MMMM Do YYYY, h:mm:ss a');
      }
  }
};
</script>


<style scoped>
.events-wrapper {
  width: 100%;
  background-color: #09121a;
  margin-bottom: 100px;
}

.row-wrap {
    margin-top: 10px;
}

.table-titles {
    border-bottom: solid 2px #00529b;
    font-size: 20px;
    height: 30px;
    margin-bottom: 20px;
}

th {
    color: #fff;
    width: 25%;
    text-transform: capitalize;
    font-family: 'Montserrat', sans-serif;
    
}

.event-key-col {
text-transform: lowercase;}



.subHeadline {
  min-width: 25%;
  display: flex;
  justify-content: center;
  white-space: nowrap;
}


tr {
    height: 30px;
    display: flex;
}

table {
    width: 100%;
    border-collapse: collapse;
}

.table-wrapper {
    width: 80%;
    margin: 0 auto;
    padding-top: 40px;
}
.vs {
  margin: 0 5px 0 10px;
  text-transform: lowercase;
}


@media (max-width: 1200px) {
      .table-wrapper {
      width: 100%;
  }
}
@media (max-width: 1080px) {
  .cards-wrapper {
        margin: 0 10px 0 15px;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-around;
  }

  .table-titles {
    display: none;
  }
    .cards {
        width: 32%;
    } 

    tr {
      height: 180px;
      flex-wrap: wrap;
      border: 1px solid #00529b;
      padding: 15px 5px;
      position: relative;
      background-color: rgba(0,82,155,0.2);
      padding-bottom: 35px;
    }

  .event-key-col {
    order: 4;
    font-size: 12px;
    position: absolute;
    bottom: 15px;
    right: 0;
  }

  .event-headline {
    order: 1;
    font-size: 14px;
  }

  .subHeadline {
    order: 2;  
    
    font-size: 25px;
    flex-direction: column;

  }

  .event-start-time {
    order: 3;
  }

    th {
      width: 100%;
    }
  .nav {
    width: 100%;
  }

}
  

</style>