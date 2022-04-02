<template>
  <!--begin::Header-->
  <div
    id="kt_header"
    style=""
    class="header align-items-stretch bg-white shadow ms-5 me-5"
  >
    <!--begin::Container-->
    <div
      :class="{
        'container-fluid': headerWidthFluid,
        'container-xxl': !headerWidthFluid,
      }"
      class="d-flex align-items-stretch"
    >
      <!--begin::Wrapper-->
      <div class="d-flex justify-content-between w-100">
        <a href="/">
          <img
            src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSGSyoCbM-QTywfVUcc3rCj6SEl7eo95zYgzC2uFgr5GQ8vt3m85ESGm0mSO6reh7I-ejw&usqp=CAU"
            alt=""
            srcset=""
            class="logo"
          />
        </a>
        <div class="d-flex align-items-stretch">
          <!--begin::Navbar-->
          <div class="d-flex align-items-stretch" id="kt_header_menu_nav">
            <PrimaryMenu />
          </div>
          <!--end::Navbar-->

          <!--begin::Connexion-->
          <div class="d-flex align-items-stretch flex-shrink-0">
            <Connexion />
          </div>
          <!--end::Connexion-->
        </div>
      </div>
      <!--end::Wrapper-->
    </div>
    <!--end::Container-->
  </div>
  <!--end::Header-->
</template>

<script lang="ts">
import { defineComponent } from "vue";
// import KTTopbar from "@/layout/header/Topbar.vue";
// import KTMenu from "@/layout/header/Menu.vue";
import PrimaryMenu from "@/layout/header/PrimaryMenu.vue";
import Connexion from "@/layout/header/Connexion.vue";

import {
  headerWidthFluid,
  headerLeft,
  asideDisplay,
} from "@/core/helpers/config";

export default defineComponent({
  name: "KTHeader",
  props: {
    title: String,
  },
  components: {
    PrimaryMenu,
    Connexion,
  },
  setup() {
    return {
      headerWidthFluid,
      headerLeft,
      asideDisplay,
    };
  },
});
</script>
<style scoped>
.header {
  border-radius: 10rem;
  padding: 1rem 0;
  height: 90px;
  margin-top: 2rem;
}
.logo {
  max-height: 65px;
}
</style>
