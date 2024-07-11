<script setup>
</script>

<template>
  <div id="grid">
    <div class="grid">
      <div class="list">
        <ul>
          <li>
            <div><span>精选</span><span>猜你喜欢</span></div>
          </li>
          <li>
            <div><span>智能先锋</span><span>大电器城</span></div>
          </li>
          <li>
            <div><span>居家优品</span><span>品质生活</span></div>
          </li>
          <li>
            <div><span>超市百货</span><span>百货生鲜</span></div>
          </li>
          <li>
            <div><span>时尚达人</span><span>美妆穿搭</span></div>
          </li>
          <li>
            <div><span>进口好物</span><span>京东国际</span></div>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<style scoped>
#grid {
  display: flex;
  width: 100%;
  height: 60px;
  justify-content: center;
  background-color: #e3e4e5;
  z-index: 999;
}


.grid {
  width: 1200px;
  background-color: white;
  justify-self: center;
}

.list ul {
  display: flex;
  list-style-type: none;
  padding: 0;
  justify-content: center;
}

.list li {
  justify-self: center;
  list-style: none outside none;
  cursor: pointer;
}

.list div{
  display: flex;
  flex-direction: column;
  text-align: center;
  border-left: 1px solid #e3e4e5;
  border-right: 1px solid #e3e4e5;
  padding: 0  60px;
}
.list li :hover{
  color: red;
}

.list div>span:first-child{
  font-size: 16px;
  font-weight: 700;
}
.list div>span:last-child{
  font-size: 14px;
  font-weight: 400;
  color: #999999;
}
</style>