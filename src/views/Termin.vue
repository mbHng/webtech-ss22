<script setup>
import { reactive } from 'vue'
import '@fullcalendar/core/vdom'
import FullCalendar from '@fullcalendar/vue3'
import dayGridPlugin from '@fullcalendar/daygrid'
import timeGridPlugin from '@fullcalendar/timegrid'
import listPlugin from '@fullcalendar/list'
import interactionPlugin from '@fullcalendar/interaction'

const options = reactive({
  plugins: [dayGridPlugin, timeGridPlugin, listPlugin, interactionPlugin],
  initialView: 'dayGridMonth'
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
