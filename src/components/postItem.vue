<template>
    <a 
      href="/notes/in_the_middle/" 
      class="story" 
      :class="{story_orientation_vertical: vertical, story_orientation_horizontal: !vertical}" 
      :style="{ backgroundImage: 'url(' + image + ')' }"
    >
      <span v-if="vertical" class="ratio-2-3"></span>
      <img v-else :src="image" class="story__stretch-img">
      <span class="story__lock"><i class="fas fa-lock" aria-hidden="true"></i></span>
      <span class="story__views"><i class="fas fa-eye" aria-hidden="true"></i>&nbsp;{{likes}}</span>
      <span class="story__info">
        <span class="story__title" style="font-size: 230%;">{{title}}</span>
        <div class="clearfix10"></div>
        <span v-if="subtitle" class="story__subtitle">{{subtitle}}</span>
      </span>
    </a>
</template>

<script>
export default {
  props: {
    image: { type: String, required: true },
    title: String,
    subtitle: String,
    likes: String,
    vertical: Boolean
  }
}
</script>

<style>
  .story {
    display: block;
    overflow: hidden;
    position: relative;
    width: 100%;
    min-width: 300px;
    min-height: 150px;
    background-size: cover;
    background-repeat: no-repeat;
    background-position: 50% 50%;
    -webkit-transition: all 0.1s linear;
    font-size: 26px;
    box-shadow: 10px 10px 30px #CCC;
    transition: all 0.5s;
    transform: translateZ(0);
    border-radius: 30px;
  }
  .story:hover {
    transform: scale(1.02);
    transition: all 0.2s;
  }
  .story.story_orientation_horizontal {
    width: 90%;
    max-width: 1000px;
  }
  .story.story_orientation_vertical {
    width: 20%;
    font-size: 12px;
  }
  .story_orientation_vertical {
    min-height: 350px;
    margin: 0 0 40px;
    font-size: 22px;
  }
  .story_orientation_horizontal {
    box-sizing: border-box;
    margin: 0 0 40px;
    font-size: 28px;
  }
  .story__stretch-img {
    visibility: hidden;
    width: 100%;
    min-height: 270px;
  }
  .ratio-2-3 {
    display: block;
    width: 100%;
    padding-bottom: 150%;
  }
  .story__lock {
    color: #FFF;
    position: absolute;
    top: 20px;
    left: 20px;
    font-size: 26px;
  }
  .story__views {
    color: #FFF;
    position: absolute;
    top: 20px;
    right: 20px;
    font-size: 12px;
  }
  .story__info {
    display: block;
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    color: #FFF;
    z-index: 20;
    padding: 0 20px 40px;
    box-sizing: border-box;
    text-align: center;
  }
  .story_orientation_vertical .story__info {
    background-color: #FFF;
    padding: 20px;
    text-align: left;
  }
  .story__title {
    display: inline;
    font-size: 200%;
    font-weight: 500;
    line-height: 1.3em;
    -webkit-box-decoration-break: clone;
    box-decoration-break: clone;
    background-color: #FFF;
    color: #000;
    padding: 5px 10px;
    box-sizing: border-box;
    transition: all 0.5s;
  }
  .story_orientation_vertical .story__title, .story_orientation_vertical .story__subtitle {
    background-color: transparent;
  }
  .clearfix10 {
    display: block;
    width: 100%;
    height: 10px;
    clear: both;
  }
  .story__subtitle {
    display: inline;
    font-weight: 400;
    clear: both;
    padding: 3px 10px;
    -webkit-box-decoration-break: clone;
    box-decoration-break: clone;
    background-color: #FFF;
    color: #000;
    line-height: 1.3em;
    transition: all 0.5s;
  }
  .story_orientation_vertical .story__title, .story_orientation_vertical .story__subtitle {
    background-color: transparent;
  }
  .story_orientation_vertical:hover .story__info {
    background-color: #333;
    color: #FFF;
    transition: all 0.3s;
  }
  .story:hover .story__views, .story:hover .story__lock {
      color: #333;
  }
  .story:hover .story__title {
    background-color: #333;
    color: #FFF;
    transition: all 0.3s;
  }
  .story:hover .story__subtitle {
    background-color: #333;
    color: #FFF;
    transition: all 0.3s;
  }
  .story_orientation_vertical:hover .story__title, .story_orientation_vertical:hover .story__subtitle {
    background-color: transparent;
  }
</style>