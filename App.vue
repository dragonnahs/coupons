<script>
	export default {
		onLaunch: function() {
			console.log('App Launch');
		},
		onShow: function() {
			console.log('App Show');
		},
		onHide: function() {
			console.log('App Hide');
		},
		globalData: {
			data: {
				home: {
					"tabs": [{
						"_id": "5fc4bf91fb0f85000174c4c9",
						"icon": "/static/all.png",
						"tabId": 0,
						"text": "全部"
					}, {
						"_id": "5fc4bf91fb0f85000174c4ca",
						"icon": "/static/ele.png",
						"tabId": 1,
						"text": "饿了么"
					}, {
						"_id": "5fc4bf91fb0f85000174c4cb",
						"icon": "/static/meituan.png",
						"tabId": 2,
						"text": "美团"
					}, {
						"_id": "5fc4bf91fb0f85000174c434",
						"icon": "/static/pdd_icon.png",
						"tabId": 5,
						"text": "拼多多优惠券",
						"appId": "wxe79b2252872fd7a4",
						"path": "pages/index/index"
					}],
					"coupons": [{
						"_id": "5fc4bf8ffbd6de00010be375",
						"bannerPic": "/static/coupon/ele_banner.png",
						"icon": "/static/coupon/ele.png",
						"minapp": {
							"appid": "wxece3a9a4c82f58c9",
							"path": "pages/sharePid/web/index?scene=https://s.click.ele.me/INk7htu"
						},
						"name": "饿了么红包",
						"tabId": 1,
						"type": 1,
						"url": "https://s.click.ele.me/INk7htu"
					}, {
						"_id": "5fc4bf8ffbd6de00010be376",
						"bannerPic": "/static/coupon/meituan_banner.png",
						"icon": "/static/coupon/meituan.png",
						"minapp": {
							"appid": "wx2c348cf579062e56",
							"path": "outer_packages/r2xinvite/coupon/coupon?inviteCode=NnOIp-QOs8SiYF1dcSlL5r8phPrCf6qkH7evMyjIoup2NXxNCLYcBbd3bqpv2X2IztI9wuZn13xnLXxvn8WLwvS9nd9A-rgRplYmnh8VHpdw2lsrKipLUX7Yd8kB_0ETeNnH_DULAj1PCPbSVKBeTytyPPsDMFNQRr-aXA6evvc"
						},
						"name": "美团外卖红包",
						"tabId": 2,
						"type": 1
					},{
						"_id": "5fc4bf8ffbd6de00010be377",
						"bannerPic": "/static/coupon/ele_fruit_banner.png",
						"icon": "/static/coupon/ele.png",
						"minapp": {
							"appid": "wxece3a9a4c82f58c9",
							"path": "pages/sharePid/web/index?scene=https://s.click.ele.me/8av5htu"
						},
						"name": "饿了么水果超市",
						"tabId": 1,
						"type": 1,
						"url": "https://s.click.ele.me/8av5htu"
					}]
				},
			},
		}

	};
</script>

<style>

</style>
