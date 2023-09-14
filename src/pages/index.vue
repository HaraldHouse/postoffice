<!-- eslint-disable vue/no-useless-v-bind -->
<script setup>
const url = ref()
function getImageUrl(name) {
  return new URL(`../../public/assets/${name}`, import.meta.url).href
}
</script>

<template>
  <!-- <Demo /> -->
  <full-page id="fullpage" ref="fullpage" :options="options">
    <div class="section">
      <div class="video_container relative">
        <div class="menu">
          <div class="logo">
            <span>The Post Office</span>
            <p class="mt-4">
              Where Vision Takes Flight, Frame by Frame
            </p>
          </div>
          <ul>
            <li on:click="{goto}">
              Services
            </li>
            <li>Our Team</li>
            <li>Portfolio</li>
            <li>Contact Us</li>
          </ul>
        </div>

        <svg
          class="testlogo"
          xmlns="http://www.w3.org/2000/svg"
          version="1.0"
          viewBox="0 0 375 375"
        ><path
          fill="#fff"
          d="M291 249c19-2 53-8 55-9 2-3-3-5-16-6l-13-1 9-7c4-4 8-9 8-11s2-4 5-4l15-2c11-3 15-13 8-20-3-3-3-10-3-29v-26l-14-13c-13-11-14-13-13-21 1-10 0-14-4-14-3 0-11-32-11-44s-6-13-101-16C73 23 27 23 21 26c-4 2-6 5-6 13a2871 2871 0 0 1-5 128l-1 16 13 3 13 1c0-1-5-3-11-4l-12-2 2-42C18 31 18 32 24 29c5-2 41-2 127 0l137 2c20 0 24 2 25 12a311 311 0 0 0 0 16l-3-12h-23c-15-1-22 0-22 2 0 1 2 2 5 1s9 2 20 10l17 11 6 4c3 3 4 3 4-1 0-6 4 6 4 13 0 4 0 4-2-1s-2-5-1 3c1 5 0 9-1 9s-10-7-19-16l-19-16c-7-1-9-4-9-8-1-3-1-4-2-2-2 3 6 40 10 44 1 2 9 3 23 3 20 0 21 0 21-6 0-3 1-1 2 5l7 14c4 5 4 5-3 1l-8-4c-3 0 2 5 9 8l6 2c-3-6 4-2 12 6 8 7 9 9 9 19-1 10-2 10-9 11-6 0-7-1-6-3 0-2 3-4 6-4s4-1 4-6v-6h-45c-27 0-46 1-46 2l-2 6c-1 3 1 4 7 4 5 0 7 1 7 5l4 8c3 4 3 4 5-4 1-10 5-11 30-11 16 0 17 0 22 7 3 4 6 11 6 15s1 7 4 8c6 3 7 2 3-2-2-2-2-4 2-5 2-2 3-4 2-6-1-1-3-2-4-1s-2 0-2-1c0-4 7-4 8 0l3 12 1 9-15 2-76 5c-18 1-28 3-29 5s-4 2-7 2c-4-1-6-4-8-11-6-19-18-27-36-22-7 2-10 5-15 16l-8 18c0 3-2 6-3 6l-68-9c-6-1-9-4-12-13-7-17-16-25-25-25-10 0-13 2-16 10-4 9-4 13 0 11 1-1 2 3 2 10 0 20 9 31 27 32a2448 2448 0 0 1 140 25l42 1h42Zm-39-22c-23-2-23-7 1-9 17-2 17-2 25 6l8 8-9-2-25-3Zm-61 2c-6-3-11-18-9-26s10-16 17-16c9 0 18 11 18 22 0 18-13 27-26 20Zm21-8c2-4 0-4-4-1-1 2-2 4 0 4l4-3Zm-15 1c-1-1 1-3 4-4s5-3 5-8c0-4-2-7-5-8-3 0-5-2-4-4l-4 3c-2 3-5 5-5 3s0-3-1-2v5c1 4 3 4 6 1 6-3 9-1 7 5-1 2-4 3-6 3-5-2-4 1 1 6 2 2 3 2 2 0Zm18-12c0-3-1-3-1-1v4c1 1 1 0 1-3Zm-2-8c0-3-5-6-6-5s0 3 2 5 4 2 4 0Zm-20-7c4-4 3-4 0-1l-5 4c0 2 2 1 5-3Zm-29 22h5c2 1 1 2-2 2-2 0-4-1-3-2Zm-81-6 6-9a235 235 0 0 1 54 9c1 1 3 3 5 3 9 1-24 4-47 5H77Zm159 1c-5-1-6-13-1-14l45-4 58-4c14-1 17-1 18 3 2 5-2 14-7 14-1 0-1-1 1-3 3-2-1-2-13-2-11 1-17 0-18-2 0-2-4-3-9-3h-8l8 1c5 1 8 3 8 5s4 4 11 4c7 1 4 1-9 2l-23 1c-3 1-4 0-3-2 2-4-7-5-32-2-17 1-20 5-8 6 7 1 6 1-3 2l-15-2Zm37-12h-14l7 1c8 0 11-1 7-1Zm-228 5c-5-5-6-8-5-15 2-11 5-16 13-16 5 0 13 9 10 12-1 1-2 0-2-1 0-2-1-3-3-3s-1 2 2 4c5 5 8 12 4 10-1-1-3 0-4 2-2 6-5 4-4-3s-2-11-9-12c-4-1-1 6 3 7 5 2 5 7 0 7l-4 2c0 4 8 6 13 3 6-4 6-1 1 5-6 6-8 6-15-2ZM299 95l-11-16-8-11 17 16c13 14 15 16 10 16-3 0-6-2-8-5Zm-136 95c4-9 3-11-1-2l-3 8c1 0 3-2 4-6Zm96-2c-6-2-5-6 1-4l6-2c1-2 1-3-1-2-5 4-9-1-4-5 4-2 4-4 2-6-5-5-4-7 2-4 4 2 5 1 5-2 0-2-3-3-6-3s-7-1-8-3c-2-1-3 3-2 14 0 15 0 17 5 18 3 0 4 0 0-1Zm64-3c7-2 7-2 7-14-1-18-2-20-12-18l-21 2h-12v32h15l23-2Zm-152-12c4-9 3-11-2-3l-2 8 4-5Zm63-6c2-3-1-8-4-6s-3 9 0 9l4-3Zm-101-7c0-4 0-5-1-3v6c1 1 1 0 1-3Zm1-14c0-3-1-4-2-2v5c1 1 2 0 2-3Zm-14-1a845 845 0 0 0-100-10 4656 4656 0 0 1 100 10Zm14-14c0-3-1-3-2-1v4c1 1 2 0 2-3Zm48-15c3-3 1-13-3-14-3-1-3 0-3 7 1 9 2 10 6 7Zm72-7h-27 27Zm-49-12c0-7 0-14-2-15-1-1-2 3-1 8 0 7-1 9-5 10-2 1-5-1-7-2-1-3-2-1-2 4 0 8 1 8 9 8h8V97Zm61 3c1-2 0-8-1-13-3-10-3-10-2-1 1 12 0 14-10 14-6 0-9-1-9-4-4-12-10-21-21-35-11-13-12-15-7-15 3 0 10 5 16 10 5 5 15 12 21 15l10 5-2-8-1-12c0-10-7-12-30-12h-22v9l3 28c3 17 3 18 11 20 14 3 43 2 44-1Zm-91-7c1-2 1-3-1-2-1 1-5-3-9-9-9-15-11-14-2 0 3 7 5 11 3 11-4-2-26-42-22-42 1 0 2-1 2-3s-1-2-3 0c-3 3-4 9-3 25v21l16 1c11 1 18 0 19-2Zm14-4c1-3 4-6 6-6 4 0 4 0-2-15-7-17-6-21 1-7 7 12 8 11 4-7-3-15-9-17-11-5s-1 47 2 40Zm-11-23-1-19h-14c-8-1-14 0-14 1s5 8 12 14l15 17c1 4 2-1 2-13Zm-42 3c0-2-1-3-1-1v5l1-4Zm175-29a873 873 0 0 0-94-1c12 2 97 3 94 1Zm-178-6Zm0 0"
        /></svg>
        <video
          style="object-fit: cover;"
          autoplay
          muted
          width="100%"
          height="100%"
          controls
        >
          // eslint-disable-next-line vue/no-useless-v-bind
          <source src="file.mp4" type="video/mp4">
        </video>
      </div>
    </div>
    <div class="section">
      Second section ...
    </div>
  </full-page>
</template>

<style scoped>
.video_container {
    width: 140vw;
    height: 140vh;
  }

  video {
    position: absolute;
    left: 50%; /* % of surrounding element */
    top: 50%;
    transform: translate(-50%, -50%); /* % of current element */
  }
  .menu {
    display: flex !important;
    position: fixed;
    align-items: center;
    top: 0;
    left: 0;
    -webkit-backdrop-filter: blur(20px);
    width: 100%;
    height: 100vh;
    z-index: 19;
    justify-content: space-between;
  }
  .logo {
    z-index: 9;
    width: auto;
    padding-left: 65px;
    padding-top: 5px;
    height: 96px;
    margin-left: 15px;
    background: url("/logo2.png") no-repeat 0 0px;
    background-size: 60px;
    color: white;
    font-family: "Helvetica" !important;
  }
  svg.testlogo {
    width: 600px;
    height: 600px;
    z-index: 999;
    display: none;
    position: absolute;
    top: 10px;
    left: 10px;
    opacity: 0.2;
  }
  .logo span {
    border-top: 2px solid rgba(255, 255, 255, 0.8);
    border-bottom: 2px solid rgba(255, 255, 255, 0.8);
    padding: 6px 0;
    font-size: 14px;
    text-transform: uppercase;
    font-weight: 100;
  }
  ul {
    list-style-type: none;
    color: white;
    text-transform: uppercase;
    margin-right: 20px;
    font-weight: 100;
    width: 500px;
    display: flex;
  }

  ul li {
    border-right: 1px solid rgba(255, 255, 255, 0.4);
    padding-right: 10px;
    margin-right: 10px;
  }
</style>
