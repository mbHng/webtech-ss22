<script setup>
import { reactive, ref } from 'vue'
import '@fullcalendar/core/vdom'
import FullCalendar from '@fullcalendar/vue3'
import dayGridPlugin from '@fullcalendar/daygrid'
import timeGridPlugin from '@fullcalendar/timegrid'
import listPlugin from '@fullcalendar/list'
import interactionPlugin from '@fullcalendar/interaction'

const id = ref(10)
const options = reactive({
  plugins: [dayGridPlugin, timeGridPlugin, listPlugin, interactionPlugin],
  initialView: 'dayGridMonth',
  headerToolbar: {
    left: 'prev, next today',
    center: 'title',
    right: 'dayGridMonth, dayGridWeek, listDay'
  },
  editable: true,
  selectable: true,
  weekends: true,
  select: (arg) => {
    id.value = id.value + 1

    const cal = arg.view.calendar
    cal.unselect()
    cal.addEvent({
      // eslint-disable-next-line no-template-curly-in-string
      id: '${id.value}',
      // eslint-disable-next-line no-template-curly-in-string
      title: 'New event ${id.value}',
      start: arg.start,
      end: arg.end,
      allDay: true
    })
  },
  eventClick: (arg) => {
    console.log(arg.start + arg.end)
  }
})
</script>

<!--<template>-->
<!--  <div class="termin">-->
<!--  <h1>Termin buchen</h1>-->
<!--  </div>-->
<!--</template>-->
<template>
<FullCalendar :options="options"/>
</template>
<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'Termin'
}
</script>

<style scoped>

</style>
