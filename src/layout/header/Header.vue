<template>
  <!--begin::Header-->
  <div
    id="kt_header"
    style=""
    class="header align-items-stretch bg-white shadow"
  >
    <!--begin::Container-->
    <div
      :class="{
        'container-fluid': headerWidthFluid,
        'container-xxl': !headerWidthFluid,
      }"
      class="d-flex align-items-stretch justify-content-between"
    >
      <!--begin::Aside mobile toggle-->
      <div
        class="d-flex align-items-center d-lg-none ms-n3 me-1"
        title="Show aside menu"
      >
        <div
          class="btn btn-icon btn-active-light-primary"
          id="kt_aside_mobile_toggle"
        >
          <span class="svg-icon svg-icon-2x mt-1">
            <inline-svg src="media/icons/duotune/abstract/abs015.svg" />
          </span>
        </div>
      </div>
      <!--end::Aside mobile toggle-->

      <!--begin::Mobile logo-->
      <div class="d-flex align-items-center flex-grow-1 flex-lg-grow-0">
        <a href="#" class="d-lg-none">
          <img alt="Logo" src="media/logos/logo-2.svg" class="h-30px" />
        </a>
      </div>
      <!--end::Mobile logo-->

      <!--begin::Wrapper-->
      <div
        class="
          d-flex
          align-items-stretch
          justify-content-between
          flex-lg-grow-1
        "
      >
        <img
          src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSGSyoCbM-QTywfVUcc3rCj6SEl7eo95zYgzC2uFgr5GQ8vt3m85ESGm0mSO6reh7I-ejw&usqp=CAU"
          alt=""
          srcset=""
        />
        <!--begin::Navbar-->
        <div class="d-flex align-items-stretch" id="kt_header_menu_nav">
          <PrimaryMenu />
        </div>
        <!--end::Navbar-->

        <!--begin::Topbar-->
        <div class="d-flex align-items-stretch flex-shrink-0">
          <Connexion />
        </div>
        <!--end::Topbar-->
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
</style>
