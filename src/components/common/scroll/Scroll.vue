<template>
  <div class="wrapper" ref="wrapper">
    <div class="content">
      <slot></slot>
    </div>
  </div>

</template>

<script>
  import BScroll from 'better-scroll'

  export default {
    name: "Scroll",
    props:{
      probeType: {
        type: Number,
        default: 0
      },
      pullUpLoad: {
        type: Boolean,
        default: false
      }
    },
    data(){
      return {
         scroll : null
      }
    },
    mounted() {
      this.scroll = new BScroll(this.$refs.wrapper,{
        click:true,
        probeType: this.probeType,
        pullUpLoad: this.pullUpLoad
      })
      // 监听滚动位置
      if (this.probeType ===2 || this.probeType ===3){
        this.scroll.on('scroll', (position) => {
          // console.log(position);
          this.$emit('scroll', position)
        })
      }

      // 监听上拉加载
      if (this.pullUpLoad){
        this.scroll.on('pullingUp',()=>{
          // console.log('上拉加载更多');
          this.$emit('pullingUp')
          setTimeout(()=>{
            this.scroll.finishPullUp()
          },2000)
        })
      }
    },
    methods:{
      scrollTo(x,y,time = 500){
        this.scroll && this.scroll.scrollTo && this.scroll.scrollTo(x,y,time)
      },
      refresh(){
        this.scroll && this.scroll.refresh()
      }
    }
  }
</script>

<style scoped>

</style>
