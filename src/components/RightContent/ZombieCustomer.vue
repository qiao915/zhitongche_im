<template lang="html">
  <div class="single-chat">

    <section class="chat-container">
      <ZombieFans></ZombieFans>
    </section>

    <aside class="chat-target-info">
      <span v-if="show_memberDetail">
        <UserDetail></UserDetail>
      </span>
    </aside>
  </div>
</template>

<script>
import ZombieFans from '../RightDetail/ZombieFans'
import UserDetail from '../RightInfo/UserDetail'
import { mapGetters } from 'vuex'

export default {
  components: {
    ZombieFans,
    UserDetail
  },
  computed: {
    ...mapGetters([
      'show_memberDetail'
    ]),
  }
}
</script>

<style lang="less" scoped>
.single-chat {
  width: 100%;
  height: 100%;
  position: relative;
  display: flex;

  .chat-container {
    width: 1px;
    height: 100%;
    flex: 1;
  }

  .chat-target-info {
    width: 270px;
    height: 100%;
    position: relative;
    border-left: 1px solid #cac5c5;
  }
}
</style>
