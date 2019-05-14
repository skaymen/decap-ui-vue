<template>
<v-app>
  <div class="platforms">
    <h2>
      Platforms
      <v-text-field v-model="search" append-icon="search" label="Search" single-line hide-details/>
    </h2>

    <v-data-table
      :headers="headers"
      :items="platforms"
      :search="search"
      class="table"
    >
      <template v-slot:items="props">
        <td class="text-xs-left">{{ props.item.platform }}</td>
        <td class="text-xs-left">{{ props.item.location_number }}</td>
        <td class="text-xs-left">{{ props.item.location_name }}</td>
        <td class="text-xs-left">{{ props.item.active }}</td>
        <td class="text-xs-left">{{ props.item.transmission_id }}</td>
        <td class="text-xs-left">{{ props.item.description }}</td>
      </template>
      <template v-slot:no-results>
        <v-alert
          :value="true"
          color="error"
          icon="warning"
        >Your search for "{{ search }}" found no results.</v-alert>
      </template>
    </v-data-table>
  </div>
  </v-app>
</template>

<script>
import platformdata from "../data/platformdata.json";

export default {
  data() {
    return {
      search: "",
      headers: [
        { text: "Platform", value: "platform" },
        { text: "Location Number", value: "location_number" },
        { text: "Location Name", value: "location_name" },
        { text: "Active", value: "active" },
        { text: "Transmission ID", value: "transmission_id" },
        { text: "Description", value: "description" }
      ],
      platforms: platformdata,
      value: []
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
  margin-right: 1vw;
  font-size: 3em;
}

.table {
  margin-right: 1vw;
}

</style>