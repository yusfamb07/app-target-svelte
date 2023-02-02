<script>
	import { onMount } from 'svelte';
	onMount(async () => {
		const ApexCharts = (await import('apexcharts')).default;
		var options = {
			legend: {
				show: true,
				position: 'right',
				markers: {
					fillColors: ['#D58407', '#17665D', '#1A4C7A', '#903C29'],
					radius: 0,
					customHTML: undefined,
					onClick: undefined,
					offsetX: 0,
					offsetY: 0,
					width: 19,
					height: 6
				},
				labels: {
					colors: ['#fff'],
					useSeriesColors: false
				}
			},
			dataLabels: {
				enabled: false
			},
			stroke: {
				show: false
			},
			fill: {
				colors: ['#D58407', '#17665D', '#1A4C7A', '#903C29']
			},
			series: [44, 55, 13, 43],
			chart: {
				width: 460,
				type: 'pie'
			},

			labels: [
				'Lawful Interception Request',
				'Geolocation Request',
				'Telecomunication Request',
				'All Pending Request'
			],
			responsive: [
				{
					breakpoint: 480,
					options: {
						chart: {
							width: 200
						},
						legend: {
							show: false,
							position: 'bottom',
							labels: {
								colors: undefined,
								useSeriesColors: false
							}
						}
					}
				}
			]
		};
		const chart = new ApexCharts(document.querySelector('#chartPie'), options);
		chart.render();
	});

	// var chart =
</script>

<div id="chartPie" />
