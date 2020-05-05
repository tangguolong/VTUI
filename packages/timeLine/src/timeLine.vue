<template>
  <div class="w__timeLine">
    <!-- <textarea @input="handleInput"
              v-bind="$props"
              class="w__limit--textarea"
              :class="{'w__limit-over': isOver}"
              :value="currentValue">
    </textarea>
    <span class="w__limit--text">
      {{isOver ? '已超出' : '还可以输入'}}<span class="w__limit--num"
            :class="{'w__limit--num-over': isOver}">{{num}}</span>个字
    </span> -->
    <a v-for="(item,index) in timeListData"
       :key="index"
       class="w__timeLine--item">
      <div class="w__timeLine--line"></div>
      <div class="w__timeLine--dot w__timeLine--active"></div>
      <div class='w__timeLine--cbox'>
        <!-- <div class='w__timeLine--box '
             :style="`--i:`+index"
             style="animation: toLeft 1s ease-in calc(.1s*var(--i));"> -->
        <div class='w__timeLine--box '
             :style="`--i:`+index"
             style="animation: toLeft 1s ease-in">
          <div>{{item.name}}</div>
          <div>{{item.time}}</div>
        </div>
      </div>
    </a>
  </div>
</template>
<script>
export default {

  name: 'TimeLine',

  // props: {
  //   placeholder: {
  //     type: String,
  //     default: '请输入内容'
  //   },
  //   rows: {
  //     type: Number,
  //     default: 4
  //   },
  //   maxLen: {
  //     type: Number,
  //     default: 20
  //   },
  //   isCut: {
  //     type: Boolean,
  //     default: false
  //   },
  //   value: {
  //     type: [String, Number],
  //     default: ''
  //   }
  // },
  data () {
    return {
      isOver: false,
      num: this.maxLen,
      currentValue: '',
      timeListData: [
        {
          name: 'date',
          time: new Date()
        },
        {
          name: 'date',
          time: new Date()
        },
        {
          name: 'date',
          time: new Date()
        }

      ]
    }
  },
  methods: {
    // handleInput (event) {
    //   const value = event.target.value
    //   this.$emit('input', value)
    //   this.setCurrentValue(value)
    //   this.$emit('change', value)
    // },
    // setCurrentValue (value) {
    //   if (value === this.currentValue) return
    //   this.currentValue = value
    //   if (this.currentValue.length <= this.maxLen) {
    //     this.isOver = false
    //     this.num = this.maxLen - this.currentValue.length
    //   } else {
    //     if (this.isCut) {
    //       this.currentValue = this.currentValue.substring(0, this.maxLen)
    //       this.num = this.currentValue.length - this.maxLen
    //       return
    //     }
    //     this.isOver = true
    //     this.num = this.currentValue.length - this.maxLen
    //     this.$emit('overText', this.currentValue)
    //   }
    // }
  },
  watch: {
  }
}
</script>