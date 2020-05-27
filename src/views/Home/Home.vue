<template>
  <div id="Home">
    <!--导航栏-->
    <nav-bar class="home-nav"><div slot="center" >购物街</div></nav-bar>
    <tab-control class="tab-control"
                 :titles="['流行','新款','精选']"
                 @tabClick="tabClick"
                 ref="tabControl1" v-show="isShowTabControl"></tab-control>
    <scroll class="content"
            ref="scroll"
            :probe-type="3"
            :pull-up-load="true"
            @scroll="contentScroll"
            @pullingUp="contentPullingUp">
      <!--首页轮播图-->
      <home-swiper :banners="banners"
                   @swiperImageLoad="swiperImageLoad"></home-swiper>
      <!--首页推荐-->
      <recommend-view :recommends="recommends"></recommend-view>
      <!--本周流行-->
      <feature-view></feature-view>
      <!--分页tabControl-->
      <tab-control :titles="['流行','新款','精选']"
                   @tabClick="tabClick"
                   ref="tabControl2"></tab-control>
      <!--商品展示-->
      <goods-list :goods="showGoods"></goods-list>
      <ul>
        <li>哈哈哈哈哈哈哈哈哈哈哈1</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈2</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈3</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈4</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈5</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈6</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈7</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈8</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈9</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈10</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈11</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈12</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈13</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈14</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈15</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈16</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈17</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈18</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈19</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈20</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈21</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈22</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈23</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈24</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈25</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈26</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈27</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈28</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈29</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈30</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈31</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈32</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈33</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈34</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈35</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈36</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈37</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈38</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈39</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈40</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈41</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈42</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈43</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈44</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈45</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈46</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈47</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈48</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈49</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈50</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈51</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈52</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈53</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈54</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈55</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈56</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈57</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈58</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈59</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈60</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈61</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈62</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈63</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈64</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈65</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈66</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈67</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈68</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈69</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈70</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈71</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈72</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈73</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈74</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈75</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈76</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈77</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈78</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈79</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈80</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈81</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈82</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈83</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈84</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈85</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈86</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈87</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈88</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈89</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈90</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈91</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈92</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈93</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈94</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈95</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈96</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈97</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈98</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈99</li>
        <li>哈哈哈哈哈哈哈哈哈哈哈100</li>
      </ul>
    </scroll>
    <back-top @click.native="backClick" v-show="isShowBackTop"></back-top> <!--.native 监听组件的根元素的原生事件-->
  </div>
</template>

<script>
  import HomeSwiper from "./childComps/HomeSwiper";
  import RecommendView from "./childComps/RecommendView";
  import FeatureView from "./childComps/FeatureView";

  import NavBar from "components/common/navbar/NavBar";
  import Scroll from "components/common/scroll/Scroll";
  import TabControl from "components/content/TabControl/TabControl";
  import GoodsList from "components/content/goods/GoodsList";
  import BackTop from "components/content/backTop/BackTop";

  import {getHomeMultidate, getHomeGoods} from "network/home";
  import {debounce} from "common/utils";

  export default {
    name: "Home",
    components:{
      NavBar,
      HomeSwiper,
      RecommendView,
      FeatureView,
      TabControl,
      GoodsList,
      Scroll,
      BackTop
    },
    data(){
      return{
        result:null,
        banners:[],
        recommends:[],
        goods:{
          'pop':{page:0, list: []},
          'new':{page:0, list: []},
          'sell':{page:0, list: []}
        },
        currentType: 'pop',  /*当前选择的商品类型*/
        isShowBackTop:false,
        tabOffsetTop: 0,
        isShowTabControl: false
      }
    },
    computed:{
      // 返回需要展示的商品列表
      showGoods(){
        return this.goods[this.currentType].list
      }
    },
    created() {
      // 1、请求首页轮播数据
      this.getHomeMultidate()

      // 2、请求首页商品数据
      // this.getHomeGoods('pop')
      // this.getHomeGoods('new')
      // this.getHomeGoods('sell')
    },
    mounted() {
      // 防抖处理
      const refresh = debounce(this.$refs.scroll.refresh,50)
      this.$bus.$on('itemImageLoad',()=>{
        // this.$refs.scroll.refresh()
        refresh()
      })
    },
    methods:{
      /**
       * 网络请求相关
       */
      getHomeMultidate(){
        getHomeMultidate().then( res=>{
          console.log(res);
          this.result = res
          this.banners = res.data.banner.list
          this.recommends = res.data.recommend.list
        })
      },
      getHomeGoods(type) {
        const page = this.goods[type].page + 1;
        getHomeGoods(type, page)().then(res=>{
          this.goods[type].list.push(...res.data.list)
        });
        this.goods[type].page += 1
      },
      /**
       * 事件监听相关
       */
      tabClick(index){
        switch (index) {
          case 0:
            this.currentType = 'pop';
            break
          case 1:
            this.currentType = 'new';
            break
          case 2:
            this.currentType = 'sell';
            break
        }
        this.$refs.tabControl1.currentIndex = index
        this.$refs.tabControl2.currentIndex = index
      },
      backClick(){
        this.$refs.scroll.scrollTo(0,0,500)
      },
      contentScroll(position){
        this.isShowBackTop = -position.y > 1000
        this.isShowTabControl = -position.y > this.tabOffsetTop
      },
      contentPullingUp(){
        // console.log('上拉加载更多');
        getHomeGoods(this.currentType)
      },
      swiperImageLoad(){
        this.tabOffsetTop = this.$refs.tabControl2.$el.offsetTop
      }
    }
  }
</script>

<style scoped>
  #Home{
    /*padding-top: 44px;*/

    height: 100vh;
    position: relative;
  }
 .home-nav {
   background-color: var(--color-tint);
   color: white;

   /*position: fixed;*/
   /*left: 0;*/
   /*right: 0;*/
   /*top: 0;*/
   /*z-index: 9;*/
 }

  .img{
    height: 40px;
  }

  /*.tab-control{*/
  /*  position: sticky;  !*设置停留*!*/
  /*  top: 44px;*/
  /*  z-index: 9;*/
  /*}*/
  .content {
    /*height: 400px;*/
    overflow: hidden;
    position: absolute;
    top: 44px;
    bottom: 49px;
    left: 0px;
    right: 0px;
  }
  .tabControl {
    position: relative;
    z-index: 9;
  }
  /*.content{*/
  /*  height: calc(100% - 93px);*/
  /*  overflow: hidden;*/
  /*  margin-top: 44px;*/
  /*}*/

  .tab-control{
    position: relative;
    z-index: 9;
  }
</style>
