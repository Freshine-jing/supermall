<template>
  <div>
    <h2>This is Category</h2>
    <div class="wrapper" ref="aaa">
      <ul class="content">
          <button @click="btnClick">button</button>
        <li>hhh1</li>
        <li>hhh2</li>
        <li>hhh3</li>
        <li>hhh4</li>
        <li>hhh5</li>
        <li>hhh6</li>
        <li>hhh7</li>
        <li>hhh8</li>
        <li>hhh9</li>
        <li>hhh10</li>
        <li>hhh11</li>
        <li>hhh12</li>
        <li>hhh13</li>
        <li>hhh14</li>
        <li>hhh15</li>
        <li>hhh16</li>
        <li>hhh17</li>
        <li>hhh18</li>
        <li>hhh19</li>
        <li>hhh20</li>
        <li>hhh21</li>
        <li>hhh22</li>
        <li>hhh23</li>
        <li>hhh24</li>
        <li>hhh25</li>
        <li>hhh26</li>
        <li>hhh27</li>
        <li>hhh28</li>
        <li>hhh29</li>
        <li>hhh30</li>
        <li>hhh31</li>
        <li>hhh32</li>
        <li>hhh33</li>
        <li>hhh34</li>
        <li>hhh35</li>
        <li>hhh36</li>
        <li>hhh37</li>
        <li>hhh38</li>
        <li>hhh39</li>
        <li>hhh40</li>
        <li>hhh41</li>
        <li>hhh42</li>
        <li>hhh43</li>
        <li>hhh44</li>
        <li>hhh45</li>
        <li>hhh46</li>
        <li>hhh47</li>
        <li>hhh48</li>
        <li>hhh49</li>
        <li>hhh50</li>
        <li>hhh51</li>
        <li>hhh52</li>
        <li>hhh53</li>
        <li>hhh54</li>
        <li>hhh55</li>
        <li>hhh56</li>
        <li>hhh57</li>
        <li>hhh58</li>
        <li>hhh59</li>
        <li>hhh60</li>
        <li>hhh61</li>
        <li>hhh62</li>
        <li>hhh63</li>
        <li>hhh64</li>
        <li>hhh65</li>
        <li>hhh66</li>
        <li>hhh67</li>
        <li>hhh68</li>
        <li>hhh69</li>
        <li>hhh70</li>
        <li>hhh71</li>
        <li>hhh72</li>
        <li>hhh73</li>
        <li>hhh74</li>
        <li>hhh75</li>
        <li>hhh76</li>
        <li>hhh77</li>
        <li>hhh78</li>
        <li>hhh79</li>
        <li>hhh80</li>
        <li>hhh81</li>
        <li>hhh82</li>
        <li>hhh83</li>
        <li>hhh84</li>
        <li>hhh85</li>
        <li>hhh86</li>
        <li>hhh87</li>
        <li>hhh88</li>
        <li>hhh89</li>
        <li>hhh90</li>
        <li>hhh91</li>
        <li>hhh92</li>
        <li>hhh93</li>
        <li>hhh94</li>
        <li>hhh95</li>
        <li>hhh96</li>
        <li>hhh97</li>
        <li>hhh98</li>
        <li>hhh99</li>
        <li>hhh100</li>
      </ul>
    </div>
  </div>
</template>

<script>
import BScroll from "better-scroll";

export default {
  name: "category",
  data() {
    return {
      scroll: null,
    };
  },
  methods: {
      btnClick() {
          console.log('btnClick')
      }
  },
  mounted() {
    //   console.log(this.$refs.aaa)
    // this.scroll = new BScroll(this.$refs.aaa, {});
    // console.log(document.querySelector(".wrapper"));
    this.scroll = new BScroll(document.querySelector(".wrapper"), {
        probeType: 3,
        pullUpLoad: true,
        // click: false
    });
    this.scroll.on('scroll', (position) => {
        // console.log(position)

    })
    this.scroll.on('pullingUp', () => {
        console.log('upload more')
    })
  },
};
</script>

<style scoped>
.wrapper {
  height: 200px;
  top: 20px;
  left: 0;
  right: 0;
  background-color: pink;
  position: relative;
  overflow: hidden;
}
</style> 