<template>
	<v-app>
		<ligthbar></ligthbar>
			<nuxt />
	</v-app>
</template>

<script>
	import toolbar from '~/components/navbar/toolbar'
	import drawer from '~/components/navbar/drawer'
	import ligthbar from '~/components/navbar/ligthbar'
	export default {
		data() {
			return {
				clipped: false,
				fixed: false,
				items: [
					{ icon: 'apps', title: 'Welcome', to: '/' },
					{ icon: 'bubble_chart', title: 'Inspire', to: '/inspire' }
				],
				drawer_props:{
					drawer: null,
					title: 'News page',
					items: [
								{ title: 'Home', icon: 'dashboard' },
								{ title: 'About', icon: 'question_answer' }
						],
					social:[
						{link: '/', img: 'https://upload.wikimedia.org/wikipedia/commons/thumb/f/fb/Facebook_icon_2013.svg/300px-Facebook_icon_2013.svg.png'},
						{link: '/home', img: 'https://pbs.twimg.com/profile_images/506125314469023744/WULlA9EJ.png'},
						{link: '/home2', img: 'http://pluspng.com/img-png/instagram-png-instagram-png-logo-1455.png'},
					]
				}
			}
		},
		components:{
			drawer,
			toolbar,
			ligthbar
		}
	}
</script>
