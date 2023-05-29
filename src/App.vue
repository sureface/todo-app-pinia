<template>
  <div id="app">

    <Modal />

    <div class="wrapper">
      <bg-video />

      <Table />
    </div>
  </div>
</template>

<script>

import BgVideo from "@/components/bgVideo";
import Table from "@/components/table";
import Modal from "@/components/modal";
export default {
  name: 'App',
  components: {BgVideo, Table, Modal},
}
</script>

<style>

</style>
