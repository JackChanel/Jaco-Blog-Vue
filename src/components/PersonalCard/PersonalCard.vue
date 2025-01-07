<template>
  <div class="CardWrapper h-[28rem] w-full rounded-2xl relative shadow-xl mb-8">
    <div
      class="ob-gradient-cut-plate absolute bg-black/90 rounded-xl opacity-90 flex justify-center items-center pt-4 px-6 shadow-lg hover:shadow-2xl duration-300"
    >
      <div
        class="profile absolute w-full flex flex-col justify-center items-center"
      >
        <div class="flex flex-col justify-center items-center">
          <img
            class="ob-avatar diamond-avatar"
            v-if="myAvatar"
            :src="myAvatar"
            alt="myAvatar"
          />
          <h2 class="text-center pt-2 text-3xl font-semibold text-white">
            Jack Chanel
          </h2>
          <span class="UnderLine h-1 w-24 rounded-full mt-2" />
        </div>
        <div
          class="h-full w-full flex flex-col flex-1 justify-center items-center"
        >
          <div
            class="flex-1 pt-6 px-8 w-full text-sm leading-8 text-center text-white"
          >
            <span>Programming a piece of art.</span>
            <p>用<span>匠人精神</span>开发出<span>艺术</span>。</p>
          </div>

          <SocialChannels />
          <DataStatistics />
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
import myAvatar from 'assets/avatar.png';
defineOptions({
  name: 'PersonalCard',
});
</script>

<style lang="scss" scoped>
.CardWrapper {
  background: linear-gradient(
    130deg,
    rgb(36, 198, 220),
    rgb(84, 51, 255) 41.07%,
    rgb(255, 0, 153) 76.05%
  );
}
.profile {
  top: -7%;
  height: 100%;
  max-height: 100%;
}
.ob-gradient-cut-plate {
  top: 8%;
  width: calc(100% - 0.5rem);
  height: calc(92% - 0.5rem);
  margin: 0.25rem;
}
.ob-avatar {
  margin: 0;
  height: 6rem;
  width: 6rem;
  --tw-shadow: 0 20px 25px -5px rgb(0 0 0 / 0.1),
    0 8px 10px -6px rgb(0 0 0 / 0.1);
  --tw-shadow-colored: 0 20px 25px -5px var(--tw-shadow-color),
    0 8px 10px -6px var(--tw-shadow-color);
  box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000),
    var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow);
}
.diamond-avatar {
  -webkit-clip-path: polygon(50% 3%, 91% 25%, 91% 75%, 50% 97%, 9% 75%, 9% 25%);
  clip-path: polygon(50% 3%, 91% 25%, 91% 75%, 50% 97%, 9% 75%, 9% 25%);
}
.UnderLine {
  background: linear-gradient(
    130deg,
    rgb(36, 198, 220),
    rgb(84, 51, 255) 41.07%,
    rgb(255, 0, 153) 76.05%
  );
}
</style>
