<script>
// Your imports and setup code

// Import the file you want to download
import T2324_Detailed_Design_Report from "../docs/T2324_Detailed_Design_Report.pdf";
import T2324_Analysis_and_Requirements_Report from "../docs/T2324_Analysis_and_Requirements_Report.pdf";
import T2324_Project_Final_Report from "../docs/T2324_Project_Final_Report.pdf";
import T2324_Project_Specification_Report from "../docs/T2324_Project_Specification_Report.pdf";
import Final_Presentation from "../docs/Final_Presentation.pdf";

export const download_T2324_Detailed_Design_Report = () => {
  const link = document.createElement("a");
  link.href = T2324_Detailed_Design_Report;
  link.download = "T2324_Detailed_Design_Report.pdf";
  document.body.appendChild(link);
  link.click();
  document.body.removeChild(link);
};

export const download_T2324_Analysis_and_Requirements_Report = () => {
  const link = document.createElement("a");
  link.href = T2324_Analysis_and_Requirements_Report;
  link.download = "T2324_Analysis_and_Requirements_Report.pdf";
  document.body.appendChild(link);
  link.click();
  document.body.removeChild(link);
};

export const download_T2324_Project_Final_Report = () => {
  const link = document.createElement("a");
  link.href = T2324_Project_Final_Report;
  link.download = "T2324_Project_Final_Report.pdf";
  document.body.appendChild(link);
  link.click();
  document.body.removeChild(link);
};

export const download_T2324_Project_Specification_Report = () => {
  const link = document.createElement("a");
  link.href = T2324_Project_Specification_Report;
  link.download = "T2324_Project_Specification_Report.pdf";
  document.body.appendChild(link);
  link.click();
  document.body.removeChild(link);
};

export const download_Final_Presentation = () => {
  const link = document.createElement("a");
  link.href = Final_Presentation;
  link.download = "Final_Presentation.pdf";
  document.body.appendChild(link);
  link.click();
  document.body.removeChild(link);
};
</script>

<template>
  <div class="container position-sticky z-index-sticky top-0">
    <div class="row">
      <div class="col-12">
        <NavbarDefault dark :sticky="true" />
      </div>
    </div>
  </div>
  <Header>
    <div
      class="page-header min-vh-85"
      :style="`background-image: url(${news5});`"
      loading="lazy"
    >
      <div class="container">
        <div class="row">
          <div
            class="col-xl-12 col-lg-10 col-md-7 text-center mx-auto position-relative"
          >
            <h1
              class="main-heading"
              :style="{
                display: 'inline-block',
                color: 'white',
                fontWeight: 'bold',
                fontFamily: 'Abril Fatface',
              }"
            >
              IMPARTIAL
            </h1>
            <p
              :style="{
                fontWeight: '1000',
                color: 'white',
                fontWeight: 'bold',
                fontSize: '1.5vw',
                fontFamily: 'Bebas Neue',
              }"
            >
              CS491 Senior Design Project I - CS492 Senior Design Project II / Computer Science / Bilkent
              University
            </p>
          </div>
        </div>
      </div>
    </div>
  </Header>

  <div
    class="container-fluid mt-sm-5 border-radius-xl"
    :style="{
      background: 'linear-gradient(195deg, rgb(66, 66, 74), rgb(25, 25, 25))',
    }"
  >
    <div
      class="page-header py-6 py-md-5 my-sm-3 mb-3 border-radius-xl"
      :style="{
        backgroundImage: `url(${wavesWhite})`,
      }"
      loading="lazy"
    >
      <span class="mask bg-gradient-dark"></span>
      <div id="scroll1" class="container" style="width: 100rem; height: 30rem">
        <div class="row">
          <div class="d-flex justify-content-center p-5">
            <div class="col-lg-8 ms-lg-5 text-center">
              <h3 class="text-white" style="fontfamily: 'Bebas Neue'">
                About the Project
              </h3>
              <p
                class="about-project text-white font text-justify"
                style="fontfamily: 'Bebas Neue'; text-align-last: center"
              >
                We need to remain impartial right? Impartial will obtain and
                categorize news from various sources so that people can view the
                articles they want from the perspective they choose. But
                Impartial will also do more than mere classification. This
                powerful website will be able to transform articles from one
                perspective to another without needing the work of an editor.
                From a supplied article, say written from a left perspective,
                and write it in other perspectives such as center and right.
                Impartial’s vision is to foster a more balanced, informative,
                and nuanced media landscape, bridging ideological gaps, and
                encouraging a richer understanding of the world's issues.
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div
    class="card card-body blur shadow-blur mx-3 mx-md-4 mt-n6"
    style="padding-top: 50px"
  >
    <div id="scroll2" class="container" style="padding-bottom: 50px">
      <div class="row justify-content-center">
        <div
          class="col-lg-3 px-lg-1 mt-lg-0 mt-4 p-4"
          style="height: 12rem; border: 4px solid gray; margin: 0 10px"
        >
          <p class="report-title">Analysis and Requirement Report</p>
          <button
            class="download-button"
            @click="download_T2324_Analysis_and_Requirements_Report()"
          >
            Click to download !
          </button>
        </div>
        <div
          class="col-lg-2 px-lg-1 mt-lg-0 mt-4 p-4"
          style="height: 12rem; border: 4px solid gray; margin: 0 10px"
        >
          <p class="report-title">Detailed Design Report</p>
          <button
            class="download-button"
            @click="download_T2324_Detailed_Design_Report()"
          >
            Click to download !
          </button>
        </div>
        <div
          class="col-lg-2 px-lg-1 mt-lg-0 mt-4 p-4"
          style="height: 12rem; border: 4px solid gray; margin: 0 10px"
        >
          <p class="report-title">Project Specification Report</p>
          <button
            class="download-button"
            @click="download_T2324_Project_Specification_Report()"
          >
            Click to download !
          </button>
        </div>
        <div
          class="col-lg-2 px-lg-1 mt-lg-0 mt-4 p-4"
          style="height: 12rem; border: 4px solid gray; margin: 0 10px"
        >
          <p class="report-title">Project Final Report</p>
          <button
            class="download-button"
            @click="download_T2324_Project_Final_Report()"
          >
            Click to download !
          </button>
        </div>
        <div
          class="col-lg-2 px-lg-1 mt-lg-0 mt-4 p-4"
          style="height: 12rem; border: 4px solid gray; margin: 0 10px"
        >
          <p class="report-title">Final Presentation</p>
          <button
            class="download-button"
            @click="download_Final_Presentation()"
          >
            Click to download !
          </button>
        </div>
      </div>
    </div>
    <div class="container">
      <div class="row">
        <div class="d-flex flex-column w-100 text-center p-4 mb-4">
          <h3>Project's GitHub Link</h3>
          <div class="d-flex justify-content-center mt-3 flex-wrap">
            <a
              href="https://github.com/cmglmsr/ORTACI-GAZETE"
              class="mx-3"
              data-bs-toggle="tooltip"
              data-bs-placement="bottom"
              title="Vue.js - Is a Progressive JavaScript Framework"
            >
              <img
                :src="github"
                alt="title"
                loading="lazy"
                :style="{ height: '90px' }"
              />
            </a>
          </div>
        </div>
      </div>
    </div>
    <div>
      <AboutTeam id="scroll3"></AboutTeam>
    </div>
  </div>
  <DefaultFooter />
</template>

<script setup>
import { onMounted, onUnmounted } from "vue";

//example components
import NavbarDefault from "./components/NavbarDefault.vue";
import DefaultFooter from "./components/FooterDefault.vue";
import Header from "./components/Header.vue";
import FilledInfoCard from "./components/FilledInfoCard.vue";
import AboutTeam from "./components/AboutTeam.vue";

//images
import github from "@/assets/img/unnamed.png";

import news5 from "@/assets/img/news5.jpg";

//hooks
const body = document.getElementsByTagName("body")[0];
onMounted(() => {
  body.classList.add("presentation-page");
  body.classList.add("bg-gray-200");
});
onUnmounted(() => {
  body.classList.remove("presentation-page");
  body.classList.remove("bg-gray-200");
});
</script>

<style>
.report-title {
  text-align: center;
  font-size: 1rem;
  color: #333;
  margin-bottom: 15px;
}

.download-button {
  display: block;
  margin: 0 auto;
  padding: 10px 20px;
  font-size: 1rem;
  color: #fff;
  background-color: #333;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s;
}

.download-button:hover {
  background-color: #0056b3;
}
</style>
