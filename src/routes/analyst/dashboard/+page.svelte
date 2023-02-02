<script>
	import PieChart from '../../../compenents/PieChart.svelte';
	import BarChart from '../../../compenents/BarChart.svelte';
	import { onMount } from 'svelte';

	onMount(async () => {
		new DataTable('#requestlist');
	});
</script>

<div class="konten">
	<div class="container-fluid mt-3">
		<div class="row">
			<div class="col-md-3">
				<div class="card">
					<div class="card-body">
						<h6>Lawful Interception Request</h6>
						<div class="d-flex align-items-center gap-5 mt-3">
							<img class="icon-dashboard" src="/lawfull.svg" alt="" />
							<h1 id="total-lawful" class="total-lawful">56</h1>
						</div>
					</div>
				</div>
			</div>
			<div class="col-md-3">
				<div class="card">
					<div class="card-body">
						<h6>Geolocation Request</h6>
						<div class="d-flex align-items-center gap-5 mt-3">
							<img class="icon-dashboard" src="/geo.svg" alt="" />
							<h1 id="total-lawful" class="total-lawful">56</h1>
						</div>
					</div>
				</div>
			</div>
			<div class="col-md-3">
				<div class="card">
					<div class="card-body">
						<h6>Telecomunication Request</h6>
						<div class="d-flex align-items-center gap-5 mt-3">
							<img class="icon-dashboard" src="/tele.svg" alt="" />
							<h1 id="total-lawful" class="total-lawful">56</h1>
						</div>
					</div>
				</div>
			</div>
			<div class="col-md-3">
				<div class="card">
					<div class="card-body">
						<h6>Pending Request</h6>
						<div class="d-flex align-items-center gap-5 mt-3">
							<img class="icon-dashboard" src="/req.svg" alt="" />
							<h1 id="total-lawful" class="total-lawful">56</h1>
						</div>
					</div>
				</div>
			</div>
		</div>

		<div class="row mt-4">
			<div class="col-md-6">
				<div class="card" style="height: 470px;">
					<div class="card-title" />
					<div class="card-body">
						<h6>Pie Chart Request</h6>
						<div class="mt-5">
							<PieChart />
						</div>
					</div>
				</div>
			</div>
			<div class="col-md-6">
				<div class="card" style="height: 470px;">
					<div class="card-body">
						<div class="d-flex justify-content-between">
							<h6>Most Request by Binda</h6>
							<h6>Lawful Interception Request <img src="/down.png" alt="" /></h6>
						</div>
						<div class="mt-3">
							<BarChart />
						</div>
					</div>
				</div>
			</div>
		</div>

		<div class="row mt-4">
			<div class="col-md-12">
				<div class="card">
					<div class="card-body">
						<div class="d-flex justify-content-between mb-3">
							<h6>Request List</h6>
							<div class="d-flex">
								<form action="">
									<input type="date" name="" id="" />
								</form>
							</div>
						</div>
						<table id="requestlist" class="table table-striped mb-5 mt-5" style="width:100%">
							<thead>
								<tr>
									<th>No</th>
									<th>Binda</th>
									<th>Lawful Request</th>
									<th>Geolocation Request</th>
									<th>CDR Request</th>
									<th>Pending</th>
								</tr>
							</thead>
							<tbody>
								<tr>
									<td>South Korea</td>
									<td>10</td>
									<td>20</td>
									<td>61</td>
									<td>25</td>
									<td>25</td>
								</tr>
								<tr>
									<td>France</td>
									<td>10</td>
									<td>20</td>
									<td>61</td>
									<td>25</td>
									<td>25</td>
								</tr>
								<tr>
									<td>Japan</td>
									<td>10</td>
									<td>20</td>
									<td>61</td>
									<td>25</td>
									<td>25</td>
								</tr>
								<tr>
									<td>Italy</td>
									<td>10</td>
									<td>20</td>
									<td>61</td>
									<td>25</td>
									<td>25</td>
								</tr>
								<tr>
									<td>Netherlands</td>
									<td>10</td>
									<td>20</td>
									<td>61</td>
									<td>25</td>
									<td>25</td>
								</tr>
								<tr>
									<td>Canada</td>
									<td>10</td>
									<td>20</td>
									<td>61</td>
									<td>25</td>
									<td>25</td>
								</tr>
								<tr>
									<td>United Kingdom</td>
									<td>10</td>
									<td>20</td>
									<td>61</td>
									<td>25</td>
									<td>25</td>
								</tr>
							</tbody>
						</table>
					</div>
				</div>
			</div>
		</div>
	</div>
</div>
