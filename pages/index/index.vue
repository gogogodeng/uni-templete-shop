<template>
	<view class="p-1">
		<u-search placeholder="日照香炉生紫烟" v-model="keyword"></u-search>
		<view class="my-1">
			<u-swiper :list="bannerlist"></u-swiper>
		</view>
		<view>
			<u-grid :border="false" :col="5">
				<u-grid-item>
					<u-icon name="photo" :size="46"></u-icon>
					<view class="grid-text">图片</view>
				</u-grid-item>
				<u-grid-item>
					<u-icon name="lock" :size="46"></u-icon>
					<view class="grid-text">锁头</view>
				</u-grid-item>
				<u-grid-item>
					<u-icon name="hourglass" :size="46"></u-icon>
					<view class="grid-text">沙漏</view>
				</u-grid-item>
				<u-grid-item>
					<u-icon name="hourglass" :size="46"></u-icon>
					<view class="grid-text">沙漏</view>
				</u-grid-item>
				<u-grid-item>
					<u-icon name="hourglass" :size="46"></u-icon>
					<view class="grid-text">沙漏</view>
				</u-grid-item>
			</u-grid>
		</view>
		<view class="my-1">
			<view class="my-1 font-md font-weight">推荐商品</view>
			<scroll-view scroll-x="true" class="scroll-row">
				<view class="scroll-row-item">
					<view class="demo-warter">
						<!-- 警告：微信小程序中需要hx2.8.11版本才支持在template中结合其他组件，比如下方的lazy-load组件 -->
						<u-lazy-load threshold="-450" border-radius="10"
							image="http://pic.sc.chinaz.com/Files/pic/pic9/202002/zzpic23325_s.jpg" :index="index">
						</u-lazy-load>
						<view class="demo-title">{{ 'dhdhdh' }}</view>
						<view class="demo-price">{{ '100' }}元</view>
						<view class="demo-tag">
							<view class="demo-tag-owner">自营</view>
							<view class="demo-tag-text">放心购</view>
						</view>
						<view class="demo-shop">{{ '2222' }}</view>
					</view>
				</view>
				<view class="scroll-row-item">
					<view class="demo-warter">
						<!-- 警告：微信小程序中需要hx2.8.11版本才支持在template中结合其他组件，比如下方的lazy-load组件 -->
						<u-lazy-load threshold="-450" border-radius="10"
							image="http://pic.sc.chinaz.com/Files/pic/pic9/202002/zzpic23325_s.jpg" :index="index">
						</u-lazy-load>
						<view class="demo-title">{{ 'dhdhdh' }}</view>
						<view class="demo-price">{{ '100' }}元</view>
						<view class="demo-tag">
							<view class="demo-tag-owner">自营</view>
							<view class="demo-tag-text">放心购</view>
						</view>
						<view class="demo-shop">{{ '2222' }}</view>
					</view>
				</view>
				<view class="scroll-row-item">
					<view class="demo-warter">
						<!-- 警告：微信小程序中需要hx2.8.11版本才支持在template中结合其他组件，比如下方的lazy-load组件 -->
						<u-lazy-load threshold="-450" border-radius="10"
							image="http://pic.sc.chinaz.com/Files/pic/pic9/202002/zzpic23325_s.jpg" :index="index">
						</u-lazy-load>
						<view class="demo-title">{{ 'dhdhdh' }}</view>
						<view class="demo-price">{{ '100' }}元</view>
						<view class="demo-tag">
							<view class="demo-tag-owner">自营</view>
							<view class="demo-tag-text">放心购</view>
						</view>
						<view class="demo-shop">{{ '2222' }}</view>
					</view>
				</view>
				<view class="scroll-row-item">
					<view class="demo-warter">
						<!-- 警告：微信小程序中需要hx2.8.11版本才支持在template中结合其他组件，比如下方的lazy-load组件 -->
						<u-lazy-load threshold="-450" border-radius="10"
							image="http://pic.sc.chinaz.com/Files/pic/pic9/202002/zzpic23325_s.jpg" :index="index">
						</u-lazy-load>
						<view class="demo-title">{{ 'dhdhdh' }}</view>
						<view class="demo-price">{{ '100' }}元</view>
						<view class="demo-tag">
							<view class="demo-tag-owner">自营</view>
							<view class="demo-tag-text">放心购</view>
						</view>
						<view class="demo-shop">{{ '2222' }}</view>
					</view>
				</view>
			</scroll-view>
		</view>
		<view class="my-1">
			<view class="my-1 font-md font-weight">限时抢购</view>
			<scroll-view scroll-x="true" class="scroll-row">
				<view class="scroll-row-item">123</view>
				<view class="scroll-row-item">123</view>
				<view class="scroll-row-item">123</view>
				<view class="scroll-row-item">123</view>
			</scroll-view>
		</view>
		<view class="my-2">
			<!-- 分类菜单 -->
			<scroll-view scroll-x="true" class="scroll-row" style="height: 200rpx;">
				<view class="scroll-row-item">123</view>
				<view class="scroll-row-item">123</view>
				<view class="scroll-row-item">123</view>
				<view class="scroll-row-item">123</view>
			</scroll-view>
		</view>
		<view class="my-1">
			<u-swiper :list="bannerlist"></u-swiper>
		</view>
		<view class="my-1">
			<!-- 推荐商品 -->
			<u-waterfall v-model="flowList" ref="uWaterfall">
				<template v-slot:left="{ leftList }">
					<view class="demo-warter" v-for="(item, index) in leftList" :key="index">
						<!-- 警告：微信小程序中需要hx2.8.11版本才支持在template中结合其他组件，比如下方的lazy-load组件 -->
						<u-lazy-load threshold="-450" border-radius="10" :image="item.image" :index="index">
						</u-lazy-load>
						<view class="demo-title">{{ item.title }}</view>
						<view class="demo-price">{{ item.price }}元</view>
						<view class="demo-tag">
							<view class="demo-tag-owner">自营</view>
							<view class="demo-tag-text">放心购</view>
						</view>
						<view class="demo-shop">{{ item.shop }}</view>
						<u-icon name="close-circle-fill" color="#fa3534" size="34" class="u-close"
							@click="remove(item.id)"></u-icon>
					</view>
				</template>
				<template v-slot:right="{ rightList }">
					<view class="demo-warter" v-for="(item, index) in rightList" :key="index">
						<u-lazy-load threshold="-450" border-radius="10" :image="item.image" :index="index">
						</u-lazy-load>
						<view class="demo-title">{{ item.title }}</view>
						<view class="demo-price">{{ item.price }}元</view>
						<view class="demo-tag">
							<view class="demo-tag-owner">自营</view>
							<view class="demo-tag-text">放心购</view>
						</view>
						<view class="demo-shop">{{ item.shop }}</view>
						<u-icon name="close-circle-fill" color="#fa3534" size="34" class="u-close"
							@click="remove(item.id)"></u-icon>
					</view>
				</template>
			</u-waterfall>
			<u-loadmore bg-color="rgb(240, 240, 240)" :status="loadStatus" @loadmore="addRandomData"></u-loadmore>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				bannerlist: [{
						image: 'https://cdn.uviewui.com/uview/swiper/1.jpg',
						title: '昨夜星辰昨夜风，画楼西畔桂堂东'
					},
					{
						image: 'https://cdn.uviewui.com/uview/swiper/2.jpg',
						title: '身无彩凤双飞翼，心有灵犀一点通'
					},
					{
						image: 'https://cdn.uviewui.com/uview/swiper/3.jpg',
						title: '谁念西风独自凉，萧萧黄叶闭疏窗，沉思往事立残阳'
					}
				],
				loadStatus: 'loadmore',
				flowList: [],
				list: [{
						price: 35,
						title: '北国风光，千里冰封，万里雪飘',
						shop: '李白杜甫白居易旗舰店',
						image: 'http://pic.sc.chinaz.com/Files/pic/pic9/202002/zzpic23327_s.jpg'
					},
					{
						price: 75,
						title: '望长城内外，惟余莽莽',
						shop: '李白杜甫白居易旗舰店',
						image: 'http://pic.sc.chinaz.com/Files/pic/pic9/202002/zzpic23325_s.jpg'
					},
					{
						price: 385,
						title: '大河上下，顿失滔滔',
						shop: '李白杜甫白居易旗舰店',
						image: 'http://pic2.sc.chinaz.com/Files/pic/pic9/202002/hpic2119_s.jpg'
					},
					{
						price: 784,
						title: '欲与天公试比高',
						shop: '李白杜甫白居易旗舰店',
						image: 'http://pic2.sc.chinaz.com/Files/pic/pic9/202002/zzpic23369_s.jpg'
					},
					{
						price: 7891,
						title: '须晴日，看红装素裹，分外妖娆',
						shop: '李白杜甫白居易旗舰店',
						image: 'http://pic2.sc.chinaz.com/Files/pic/pic9/202002/hpic2130_s.jpg'
					},
					{
						price: 2341,
						shop: '李白杜甫白居易旗舰店',
						title: '江山如此多娇，引无数英雄竞折腰',
						image: 'http://pic1.sc.chinaz.com/Files/pic/pic9/202002/zzpic23346_s.jpg'
					},
					{
						price: 661,
						shop: '李白杜甫白居易旗舰店',
						title: '惜秦皇汉武，略输文采',
						image: 'http://pic1.sc.chinaz.com/Files/pic/pic9/202002/zzpic23344_s.jpg'
					},
					{
						price: 1654,
						title: '唐宗宋祖，稍逊风骚',
						shop: '李白杜甫白居易旗舰店',
						image: 'http://pic1.sc.chinaz.com/Files/pic/pic9/202002/zzpic23343_s.jpg'
					},
					{
						price: 1678,
						title: '一代天骄，成吉思汗',
						shop: '李白杜甫白居易旗舰店',
						image: 'http://pic1.sc.chinaz.com/Files/pic/pic9/202002/zzpic23343_s.jpg'
					},
					{
						price: 924,
						title: '只识弯弓射大雕',
						shop: '李白杜甫白居易旗舰店',
						image: 'http://pic1.sc.chinaz.com/Files/pic/pic9/202002/zzpic23343_s.jpg'
					},
					{
						price: 8243,
						title: '俱往矣，数风流人物，还看今朝',
						shop: '李白杜甫白居易旗舰店',
						image: 'http://pic1.sc.chinaz.com/Files/pic/pic9/202002/zzpic23343_s.jpg'
					}
				]
			};
		},
		onLoad() {
			this.addRandomData();
		},
		onReachBottom() {
			this.loadStatus = 'loading';
			// 模拟数据加载
			setTimeout(() => {
				this.addRandomData();
				this.loadStatus = 'loadmore';
			}, 1000);
		},
		methods: {
			addRandomData() {
				for (let i = 0; i < 10; i++) {
					let index = this.$u.random(0, this.list.length - 1);
					// 先转成字符串再转成对象，避免数组对象引用导致数据混乱
					let item = JSON.parse(JSON.stringify(this.list[index]));
					item.id = this.$u.guid();
					this.flowList.push(item);
				}
			},
			remove(id) {
				this.$refs.uWaterfall.remove(id);
			},
			clear() {
				this.$refs.uWaterfall.clear();
			}
		}
	};
</script>

<style lang="scss" scoped>
	.scroll-row {
		height: 300rpx;
	}

	.scroll-row-item {
		width: 300rpx;
		height: 100%;
		// background-color: gray;
		// border: solid 1px;
	}

	.demo-warter {
		border-radius: 8px;
		margin: 5px;
		background-color: #ffffff;
		padding: 8px;
		position: relative;
	}

	.u-close {
		position: absolute;
		top: 32rpx;
		right: 32rpx;
	}

	.demo-image {
		width: 100%;
		border-radius: 4px;
	}

	.demo-title {
		font-size: 30rpx;
		margin-top: 5px;
		color: $u-main-color;
	}

	.demo-tag {
		display: flex;
		margin-top: 5px;
	}

	.demo-tag-owner {
		background-color: $u-type-error;
		color: #ffffff;
		display: flex;
		align-items: center;
		padding: 4rpx 14rpx;
		border-radius: 50rpx;
		font-size: 20rpx;
		line-height: 1;
	}

	.demo-tag-text {
		border: 1px solid $u-type-primary;
		color: $u-type-primary;
		margin-left: 10px;
		border-radius: 50rpx;
		line-height: 1;
		padding: 4rpx 14rpx;
		display: flex;
		align-items: center;
		border-radius: 50rpx;
		font-size: 20rpx;
	}

	.demo-price {
		font-size: 30rpx;
		color: $u-type-error;
		margin-top: 5px;
	}

	.demo-shop {
		font-size: 22rpx;
		color: $u-tips-color;
		margin-top: 5px;
	}
</style>
