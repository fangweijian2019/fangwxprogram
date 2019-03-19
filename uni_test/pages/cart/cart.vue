<template>
	<view>
		<checkbox-group @change="checkboxChange">
                <label class="uni-list-cell uni-list-cell-pd" v-for="item in items" :key="item.value">
                    <view><checkbox :value="item.value"  color='white' :checked="item.checked" /></view>
                    <view></view>
                </label>
            </checkbox-group>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				items: [{
                    value: 'USA',
                    name: '美国'
                },
                {
                    value: 'CHN',
                    name: '中国',
                    checked: 'true'
                },
                {
                    value: 'BRA',
                    name: '巴西'
                },
                {
                    value: 'JPN',
                    name: '日本'
                },
                {
                    value: 'ENG',
                    name: '英国'
                },
                {
                    value: 'FRA',
                    name: '法国'
                }
            ]
			};
		},
		methods:{
			 checkboxChange: function (e) {
            var items = this.items,
                values = e.detail.value;
            for (var i = 0, lenI = items.length; i < lenI; ++i) {
                items[i].checked = false;
                for (var j = 0, lenJ = values.length; j < lenJ; ++j) {
                    if (items[i].value == values[j]) {
                        items[i].checked = true;
                        break
                    }
                }
            }
        }
		}
	}
</script>

<style>
.cart_one{
	margin:10px auto;
}
.uni-checkbox-input.uni-checkbox-input-checked{
	background-color:#007AFF;
}
</style>
