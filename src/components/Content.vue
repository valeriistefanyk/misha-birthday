<template>
  <div>
    <block-alert></block-alert>
    <block-photo></block-photo>
    <block-twitter class="mt-10"></block-twitter>
    <block-youtube></block-youtube>
    <block-info></block-info>
    <block-parallax class="mt-10"></block-parallax>
    <block-gif class="mt-10"></block-gif>
  </div>
</template>

<script>
import BlockInfo from "@/components/BlockInfo";
import BlockTwitter from "@/components/BlockTwitter";
import BlockYoutube from "@/components/BlockYoutube";
import BlockPhoto from "@/components/BlockPhoto";
import BlockAlert from "@/components/BlockAlert";
import BlockParallax from "@/components/BlockParallax";
import BlockGif from "@/components/BlockGif";

export default {
  name: "Container",
  components: {
    BlockInfo,
    BlockPhoto,
    BlockTwitter,
    BlockYoutube,
    BlockAlert,
    BlockParallax,
    BlockGif,
  },
};
</script>

<style scoped>
</style>
