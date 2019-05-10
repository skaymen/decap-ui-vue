<template>
  <div class="Platforms">
    <h2>Platforms</h2>
    <v-data-table :headers="headers" :items="platforms" class="elevation-1">
      <template v-slot:items="props">
        <td class="text-xs-left">{{ props.item.platform }}</td>
        <td class="text-xs-left">{{ props.item.location_number }}</td>
        <td class="text-xs-left">{{ props.item.location_name }}</td>
        <td class="text-xs-left">{{ props.item.active }}</td>
        <td class="text-xs-left">{{ props.item.transmission_id }}</td>
        <td class="text-xs-left">{{ props.item.description }}</td>
      </template>
    </v-data-table>
  </div>
</template>

<script>
import platformdata from '../data/platformdata.json';

export default {
  data() {
    return {
      headers: [
        { text: "Platform", value: "platform" },
        { text: "Location Number", value: "location_number" },
        { text: "Location Name", value: "location_name" },
        { text: "Active", value: "active" },
        { text: "Transmission ID", value: "transmission_id" },
        { text: "Description", value: "description" }
      ],
      platforms: platformdata
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h2 {
  text-align: left;
  margin-top: 1vh;
  margin-left: 1vw;
}
</style>