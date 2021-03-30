<template>
  <div class="date-wrapper">
    <date-picker v-model="date" lang="en" type=date format="YYY-MM-dd"></date-picker>
  </div>
</template>

<script>

export default {
  name: 'Date',
  data () {
    return{
        start: '',
        end: ''
    }
  },

  methods: {
    onSubmit(e) {
      e.preventDefault()
      if(!this.date) {
          alert('Please select a start and end date...')
          return
      }
      
      const newFilter = {
          //probably wouldnt want to do this in a real app lol
          //id: Math.floor(Math.random() * 100000),
          start: this.start,
          end: this.end
      }
      this.$emit('add-new-filter', newFilter)

      this.start = ''
      this.end = ''
    }
  },
}
</script>