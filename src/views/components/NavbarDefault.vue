<script setup>
import { ref } from "vue";
import { useWindowsWidth } from "../../assets/js/useWindowsWidth";

// images
import ArrDark from "@/assets/img/down-arrow-dark.svg";
import DownArrWhite from "@/assets/img/down-arrow-white.svg";

const props = defineProps({
  action: {
    type: Object,
    route: String,
    color: String,
    label: String,
    default: () => ({
      route: "",
      color: "bg-gradient-success",
      label: "Free Download"
    })
  },
  transparent: {
    type: Boolean,
    default: false
  },
  light: {
    type: Boolean,
    default: false
  },
  dark: {
    type: Boolean,
    default: false
  },
  sticky: {
    type: Boolean,
    default: false
  },
  darkText: {
    type: Boolean,
    default: false
  }
});

// set arrow  color
function getArrowColor() {
  if (props.transparent && textDark.value) {
    return ArrDark;
  } else if (props.transparent) {
    return DownArrWhite;
  } else {
    return ArrDark;
  }
}

// set text color
const getTextColor = () => {
  let color;
  if (props.transparent && textDark.value) {
    color = "text-dark";
  } else if (props.transparent) {
    color = "text-white";
  } else {
    color = "text-white";
  }

  return color;
};

// set nav color on mobile && desktop

let textDark = ref(props.darkText);
const { type } = useWindowsWidth();


if (type.value === "mobile") {
  textDark.value = true;
} else if (type.value === "desktop" && textDark.value == false) {
  textDark.value = false;
}

function scroll(id) {
  const { type } = useWindowsWidth();

  if (type.value === "mobile" && id === "scroll3") {
    document.getElementById(id).scrollIntoView({ block: "start" });

  } else {
    document.getElementById(id).scrollIntoView({ block: "center" });

  }

  const nav = document.getElementById("navigation");
  nav.classList.remove("show");

}

</script>
<template>
  <nav
    class="navbar navbar-expand-lg top-0"
    :class="{
      'z-index-3 w-100 shadow-none navbar-transparent position-absolute my-3':
        props.transparent,
      'my-3 blur border-radius-lg z-index-3 py-2 shadow py-2 start-0 end-0 mx-4 position-absolute mt-4':
        props.sticky,
      'navbar-light bg-white py-3': props.light,
      ' navbar-dark bg-gradient-dark z-index-3 py-3': props.dark
    }"
  >
    <div
      :class="
        props.transparent || props.light || props.dark
          ? 'container'
          : 'container-fluid px-0'
      "
    >


      <button
        class="navbar-toggler shadow-none ms-2"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navigation"
        aria-controls="navigation"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon mt-2">
          <span class="navbar-toggler-bar bar1"></span>
          <span class="navbar-toggler-bar bar2"></span>
          <span class="navbar-toggler-bar bar3"></span>
        </span>
      </button>
      <div
        class="collapse navbar-collapse w-100 pt-3 pb-2 py-lg-0"
        id="navigation"
      >
        <ul class="navbar-nav navbar-nav-hover ms-auto " style="margin-right: 100%">
          <li class="nav-item mx-2">
            <a
              class="nav-link ps-2 d-flex cursor-pointer align-items-center"
              :class="getTextColor()"
              id="dropdownMenuPages"
              @click="scroll('scroll1')"
            >
              <i
                class="material-icons opacity-6 me-2 text-md"
                :class="getTextColor()"
                >class</i
              >
              About
              <img
                :src="getArrowColor()"
                alt="down-arrow"
                class="arrow ms-2 d-lg-block d-none"
              />
              <img
                :src="getArrowColor()"
                alt="down-arrow"
                class="arrow ms-1 d-lg-none d-block ms-auto"
              />
            </a>
          </li>
          <li class="nav-item mx-2">
            <a
              class="nav-link ps-2 d-flex cursor-pointer align-items-center"
              :class="getTextColor()"
              id="dropdownMenuDocs"
              @click="scroll('scroll2')"
            >
              <i
                class="material-icons opacity-6 me-2 text-md"
                :class="getTextColor()"
                >article</i
              >
              Docs
              <img
                :src="getArrowColor()"
                alt="down-arrow"
                class="arrow ms-2 d-lg-block d-none"
              />
              <img
                :src="getArrowColor()"
                alt="down-arrow"
                class="arrow ms-1 d-lg-none d-block ms-auto"
              />
            </a>
          </li>
          <li class="nav-item mx-2">
            <a
              class="nav-link ps-2 d-flex cursor-pointer align-items-center"
              :class="getTextColor()"
              id="dropdownMenuBlocks"
              @click="scroll('scroll3')"
            >
              <i
                class="material-icons opacity-6 me-2 text-md"
                :class="getTextColor()"
              >person</i
              >
              Team
              <img
                :src="getArrowColor()"
                alt="down-arrow"
                class="arrow ms-2 d-lg-block d-none"
              />
              <img
                :src="getArrowColor()"
                alt="down-arrow"
                class="arrow ms-1 d-lg-none d-block ms-auto"
              />
            </a>
          </li>
        </ul>
        <ul class="navbar-nav d-lg-block d-none">
          <li class="nav-item">
          </li>
        </ul>
      </div>
    </div>
  </nav>
  <!-- End Navbar -->

</template>


