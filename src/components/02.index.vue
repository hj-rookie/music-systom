<template>
  <div class="index-container">
    <!-- 导航区域 -->
    <div class="nav" >
      <ul>
        <li>
          <router-link to="/discovery">
            <span class="iconfont el-icon-view"></span>
            发现音乐
          </router-link>
        </li>
        <li>
          <router-link to="/playlists">
            <span class="iconfont el-icon-s-operation"></span>
            推荐歌单
          </router-link>
        </li>
        <li>
          <router-link to="/songs">
            <span class="iconfont el-icon-headset"></span>
            最新音乐
          </router-link>
        </li>
        <li>
          <router-link to="/mvs">
            <span class="iconfont el-icon-monitor"></span>
            最新MV
          </router-link>
        </li>
      </ul>
    </div>
    <!-- 主体区域 -->
    <div class="main">
      <router-view></router-view>
    </div>
    <!-- 播放标签 -->
    <div class="player">
      <!-- autoplay 自动播放 -->
      <audio :src='musicUrl' controls autoplay></audio>
    </div>
  </div>
</template>

<script>
export default {
  name: 'index',
  data() {
    return {
      musicUrl:""
    };
  }
};
</script>

<style >

</style>
