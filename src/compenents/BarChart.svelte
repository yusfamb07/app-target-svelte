<script>
	import { onMount } from 'svelte';
	onMount(async () => {
		const ApexCharts = (await import('apexcharts')).default;
		var options = {
			scaleLineColor: 'transparent',
			series: [
				{
					data: [400, 430, 448, 470, 540, 580]
				}
			],
			chart: {
				type: 'bar',
				height: 350,
				toolbar: {
					show: false
				}
			},
			plotOptions: {
				bar: {
					borderRadius: 0,
					horizontal: true
				}
			},
			fill: {
				type: 'gradient',
				colors: ['#50F8F8'],
				gradient: {
					shadeIntensity: 0.7,
					opacityFrom: 0.5,
					opacityTo: 0.9,
					stops: [0, 90, 300]
				}
			},
			grid: {
				show: true,
				borderColor: '#90A4AE',
				strokeDashArray: 0,
				position: 'back',
				xaxis: {
					lines: {
						show: false
					}
				},
				yaxis: {
					lines: {
						show: false
					}
				},
				row: {
					colors: undefined,
					opacity: 0.5
				},
				column: {
					colors: undefined,
					opacity: 0.5
				},
				padding: {
					top: 0,
					right: 0,
					bottom: 0,
					left: 0
				}
			},
			dataLabels: {
				enabled: false
			},
			xaxis: {
				categories: ['South Korea', 'Canada', 'United Kingdom', 'Netherlands', 'Italy', 'France'],

				labels: {
					show: false,
					style: {
						colors: 'white',
						fontSize: '12px',
						fontFamily: 'Chakra Petch',
						fontWeight: 400,
						cssClass: 'apexcharts-xaxis-label'
					}
				}
			},
			yaxis: {
				labels: {
					show: true,
					style: {
						colors: 'white',
						fontSize: '12px',
						fontFamily: 'Chakra Petch',
						fontWeight: 400,
						cssClass: 'apexcharts-yaxis-label'
					}
				}
			}
		};

		var chart = new ApexCharts(document.querySelector('#chartBar'), options);
		chart.render();
	});
</script>

<div id="chartBar" />
