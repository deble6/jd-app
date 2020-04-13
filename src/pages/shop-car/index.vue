<template>
  <div class="container">
  <ul class="book-list">
    <li class="book-list-item">

      <!-- 选择按钮 -->
      <div class="select-btn-box">
        <div>
          <input type="checkbox">
          <div class="action"></div>
        </div>
      </div>
      <!-- 书本信息 -->
      <div class="book-count-info">
        <img src="../../assets/book1.jpg" alt="">
        <div>
          <div>一生自在一生自在一生自在一生自在一生自在一生自在一生自在</div>
          <div>重量：0.32kg 系列：一生自在系列</div>
          <div>
            <span>￥42.80</span>
            <div class="change-count-box">
              <div>-</div>
              <div>1</div>
              <div>+</div>
            </div>
          </div>
        </div>
      </div>
    </li>
    <li class="book-list-item">
      <!-- 选择按钮 -->
      <div class="select-btn-box">
        <div>
          <input type="checkbox">
          <div class="action"></div>
        </div>
      </div>

      <!-- 书本信息 -->
      <div class="book-count-info">
        <img src="../../assets/book1.jpg" alt="">
        <div>
          <div>一生自在一生自在一生自在一生自在一生自在一生自在一生自在</div>
          <div>重量：0.32kg 系列：一生自在系列</div>
          <div>
            <span>￥56.80</span>
            <div class="change-count-box">
              <div>-</div>
              <div>1</div>
              <div>+</div>
            </div>
          </div>
        </div>
      </div>
    </li>
    <li class="book-list-item">
      <!-- 选择按钮 -->
      <div class="select-btn-box">
        <div>
          <input type="checkbox">
          <div class="action"></div>
        </div>
      </div>

      <!-- 书本信息 -->
      <div class="book-count-info">
        <img src="../../assets/book1.jpg" alt="">
        <div>
          <div>一生自在一生自在一生自在一生自在一生自在一生自在一生自在</div>
          <div>重量：0.32kg 系列：一生自在系列</div>
          <div>
            <span>￥82.80</span>
            <div class="change-count-box">
              <div>-</div>
              <div>1</div>
              <div>+</div>
            </div>
          </div>
        </div>
      </div>
    </li>
    <li class="book-list-item">
      <!-- 选择按钮 -->
      <div class="select-btn-box">
        <div>
          <input type="checkbox">
          <div class="action"></div>
        </div>
      </div>

      <!-- 书本信息 -->
      <div class="book-count-info">
        <img src="../../assets/book1.jpg" alt="">
        <div>
          <div>一生自在一生自在一生自在一生自在一生自在一生自在一生自在</div>
          <div>重量：0.32kg 系列：一生自在系列</div>
          <div>
            <span>￥22.80</span>
            <div class="change-count-box">
              <div>-</div>
              <div>1</div>
              <div>+</div>
            </div>
          </div>
        </div>
      </div>
    </li>
  </ul>
  </div>
</template>

<script>
export default {
  name: 'shop-car',
  data () {
    return {}
  }
}
</script>

<style lang="scss" scoped>
  .book-list {
    width: 95%;
    position: absolute;
    top: 60px;
    left: 50%;
    bottom: 55px;
    overflow: auto;
    transform: translate(-50%, 0);
  }

  .book-list li {
    display: flex;
    justify-content: flex-start;
    align-items: center;
    width: 100%;
    height: 150px;
    background: #fff;
    border-radius: 10px;
    padding: 10px 10px;
    box-sizing: border-box;
    margin-bottom: 10px;
  }

  .book-list li .select-btn-box {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 40px;
    height: 100%;
  }

  .book-list li .select-btn-box > div {
    position: relative;
    width: 20px;
    height: 20px;
    border: 2px solid #ddd;
    border-radius: 50%;
  }

  .book-list li .select-btn-box > div input {
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    padding: 0;
    margin: 0;
    width: 15px;
    height: 15px;
    z-index: 1;
    opacity: 0;
  }

  .book-list li .select-btn-box > div .action {
    display: none;
    position: absolute;
    width: 15px;
    height: 15px;
    border-radius: 50%;
    background: rgb(197, 156, 104);
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    z-index: 0;
  }

  .book-list li .book-count-info {
    display: flex;
    justify-content: flex-start;
    align-items: center;
    flex: 1;
    height: 100%;
  }

  .book-list li .book-count-info > img {
    height: 80%;
    vertical-align: middle;
    align-self: center;
  }

  .book-list li .book-count-info > div {

  }

  .book-list li .book-count-info > div > div:first-child {
    font-size: 14px;
    width: 100%;
    height: 40px;
    padding-left: 10px;
    box-sizing: border-box;
  }

  .book-list li .book-count-info > div > div:nth-child(2) {
    font-size: 14px;
    width: 100%;
    height: 30px;
    padding-left: 10px;
    box-sizing: border-box;
    color: #ddd;
  }

  .book-list li .book-count-info > div > div:nth-child(3) {
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: 14px;
    width: 100%;
    height: 30px;
    padding-left: 10px;
    box-sizing: border-box;
  }

  .book-list li .book-count-info > div > div:nth-child(3) .change-count-box {
    display: flex;
    height: 20px;
  }

  .book-list li .book-count-info > div > div:nth-child(3) .change-count-box div:first-child {
    width: 30px;
    height: 20px;
    text-align: center;
    line-height: 20px;
    border: 1px solid #ddd;
  }
  .book-list li .book-count-info > div > div:nth-child(3) .change-count-box div:nth-child(2) {
    width: 50px;
    height: 20px;
    text-align: center;
    line-height: 20px;
    border: 1px solid #ddd;
    border-left: none;
    border-right: none;
  }
  .book-list li .book-count-info > div > div:nth-child(3) .change-count-box div:nth-child(3) {
    width: 30px;
    height: 20px;
    text-align: center;
    line-height: 20px;
    border: 1px solid #ddd;
  }

</style>
