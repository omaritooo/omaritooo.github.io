<template>
  <div
    class="bg-purple-300 fonter"
    data-aos="fade-left"
    data-aos-delay="20"
    data-aos-duration="1000"
    data-aos-easing="ease-in-out"
  >
    <div class="title">Portfolio & Past Works</div>

    <div
      class="flex flex-col justify-center px-6 mt-10 md:flex-row rounded-t-md"
    >
      <div v-for="dum in shortDictionary" :key="dum.title" class="p-10">
        <div>
          <div class="max-w-sm overflow-hidden bg-gray-100 rounded shadow-lg">
            <a :href="dum.url">
              <img
                class="w-full transition duration-100 ease-in hover:scale-150"
                :src="require(`@/assets/${dum.thumbnail}.jpeg`)"
                alt="Sunset in the mountains"
              />
            </a>
            <div class="px-6 pt-4">
              <div class="flex flex-row mb-2 text-2xl font-bold">
                {{ dum.title }}
                <a
                  :href="dum.url"
                  class="
                    flex
                    float-right
                    mx-auto
                    transition
                    duration-500
                    ease-in-out
                    transform
                    hover:-translate-y-1
                    hover:shadow-xl
                    hover:scale-110
                    hover:bg-transparent
                  "
                >
                  <img src="../assets/repo.svg" alt=""
                /></a>
              </div>
              <!-- <p class="text-base text-gray-700">
                  Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                  Voluptatibus quia, nulla! Maiores et perferendis eaque,
                  exercitationem praesentium nihil.
                </p> -->
            </div>
            <div class="flex flex-wrap px-6 pt-2 pb-4 gap-x-2 gap-y-2">
              <div v-for="tag in dum.tags" :key="tag.name" class="flex w-min">
                <div
                  :class="tag.class"
                  class="
                    px-2
                    transition
                    duration-500
                    ease-in-out
                    transform
                    rounded-lg
                    w-min
                    hover:-translate-y-1 hover:shadow-xl hover:scale-110
                  "
                >
                  <span class="flex-wrap text-sm text-white">{{
                    tag.name
                  }}</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  computed: {
    shortDictionary() {
      return this.randomList(this.dummy).slice(0, 3);
    },
  },
  data() {
    return {
      dummy: [
        {
          title: "Tabib",
          url: "https://dev.to/arielmejiadev/use-tailwind-2-with-vue-cli-2md6",
          thumbnail: "Tabib",
          tags: [
            {
              name: "HTML5",
              class: "bg-blue-500",
            },
            {
              name: "CSS3",
              class: "bg-yellow-500",
            },
            {
              name: "JS",
              class: "bg-yellow-400",
            },
          ],
        },
        {
          title: "Techio",
          url: "https://quizzical-lamport-9ddeaf.netlify.app/",
          thumbnail: "Techio",
          tags: [
            {
              name: "HTML5",
              class: "bg-blue-500",
            },
            {
              name: "CSS3",
              class: "bg-yellow-500",
            },
            {
              name: "JS",
              class: "bg-yellow-400",
            },
            {
              name: "Tailwind",
              class: "bg-green-300",
            },
            {
              name: "Vue.JS",
              class: "bg-green-500",
            },
          ],
        },
        {
          title: "Gallart",
          url: "https://landing-page-272.netlify.app/",
          thumbnail: "Gallart",
          tags: [
            {
              name: "HTM5L",
              class: "bg-blue-500",
            },
            {
              name: "CSS5",
              class: "bg-yellow-500",
            },
            {
              name: "JS",
              class: "bg-yellow-300",
            },
            {
              name: "SASS",
              class: "bg-red-200",
            },
          ],
        },
        {
          title: "Landing",
          url: "https://landing-page-272.netlify.app/",
          thumbnail: "Product",
          tags: [
            {
              name: "HTML5",
              class: "bg-blue-500",
            },
            {
              name: "CSS5",
              class: "bg-yellow-500",
            },
            {
              name: "Tailwind",
              class: "bg-green-300",
            },
            {
              name: "JS",
              class: "bg-yellow-300",
            },
          ],
        },
      ],
    };
  },
  methods: {
    randomList: function (rand) {
      return rand.sort(function () {
        return 0.5 - Math.random();
      });
    },
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Niconne&family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;1,100;1,200;1,300;1,400;1,500;1,600;1,700&display=swap");
.title {
  font-size: 5rem;
  text-align: center;

  color: #fcedd8;
  font-family: "Niconne", cursive;
  font-weight: 700;
  text-shadow: 5px 5px 0px #eb452b, 7px 7px 0px #efa032, 10px 10px 0px #46b59b,
    12px 12px 0px #017e7f, 15px 15px 0px #052939;
}

@media only screen and (min-device-width: 375px) and (max-device-width: 812px) and (-webkit-min-device-pixel-ratio: 3) {
  .title {
    font-size: 3rem;
    text-align: center;

    color: #fcedd8;
    font-family: "Niconne", cursive;
    font-weight: 700;
    text-shadow: 5px 5px 0px #eb452b, 7px 7px 0px #efa032, 10px 10px 0px #46b59b,
      12px 12px 0px #017e7f, 15px 15px 0px #052939;
  }
}

.fonter {
  font-family: "Poppins", sans-serif;
  font-weight: 300;
}
</style>
