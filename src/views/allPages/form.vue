<template>
  <!--begin::Wrapper-->
  <div class="container">
    <div class="content-page">
      <div class="row">
        <Wizard />
      </div>
    </div>
  </div>
  <!--end::Wrapper-->
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Wizard from "@/views/crafted/pages/wizards/Vertical.vue";

export default defineComponent({
  name: "home",
  components: {
    Wizard,
  },
});
</script>
