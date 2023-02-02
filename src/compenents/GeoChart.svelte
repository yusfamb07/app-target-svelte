<script>
	import { onMount } from 'svelte';
	onMount(async () => {
		google.charts.load('current', {
			packages: ['geochart']
		});
		google.charts.setOnLoadCallback(drawRegionsMap);

		function drawRegionsMap() {
			var data = google.visualization.arrayToDataTable([
				['Province', 'Popularity'],
				['Id', 200],
				['United States', 300],
				['Brazil', 400],
				['Canada', 500],
				['France', 600],
				['RU', 700]
			]);

			var options = {
				backgroundColor: '#2F3740',
				colors: ['#000'],
				region: 'ID',
				resolution: 'provinces'
			};
			// var options = {};
			// options['region'] = 'ID';
			// options['resolution'] = 'provinces';
			// // options['width'] = '60%';
			// options['legend'] = 'none';
			// options['colors'] = '#000';
			// options['backgroundColor'] = '#2F3740';
			const chart = new google.visualization.GeoChart(document.getElementById('regions_div'));

			chart.draw(data, options);
		}
	});

	// var chart =
</script>

<div id="regions_div" style="width: 450px !important; height: 200px !important;" />
