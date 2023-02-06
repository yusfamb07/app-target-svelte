<script>
	import PieChart from '../../../compenents/PieChart.svelte';
	import BarChart from '../../../compenents/BarChart.svelte';
	import { onMount } from 'svelte';

	onMount(async () => {
		new DataTable('#requestlist');
	});
</script>

<!-- pake apex chart -->
<div class="konten">
	<div class="container-fluid mt-3">
		<div class="row">
			<div class="col-md-3">
				<div class="card">
					<div class="card-body">
						<h6>Lawful Interception Request</h6>
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
						<h6>Geolocation Request</h6>
						<div class="d-flex align-items-center gap-5 mt-3">
							<img class="icon-dashboard" src="/lawfull.svg" alt="" />
							<h1 id="total-lawful" class="total-lawful">22</h1>
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
							<h1 id="total-lawful" class="total-lawful">121</h1>
						</div>
					</div>
				</div>
			</div>
			<div class="col-md-3">
				<div class="card">
					<div class="card-body">
						<h6>Lawful Interception Request</h6>
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
							<PieChart
								fillColor={['#D58407', '#17665D', '#1A4C7A', '#903C29', '#29907D']}
								description={[
									'ideologi',
									'Politik',
									'Ekonomi',
									'Seni Budaya',
									'Pertahanan dan Keamanan'
								]}
								series={[25, 15, 15, 25, 20]}
								color={['#D58407', '#17665D', '#1A4C7A', '#903C29', '#29907D']}
							/>
						</div>
					</div>
				</div>
			</div>
			<div class="col-md-6">
				<div class="card" style="height: 470px;">
					<div class="card-body">
						<div class="d-flex justify-content-between">
							<h6>Most Request by Binda</h6>
							<h6>Binda Jakarta <img src="/down.png" alt="" /></h6>
						</div>
						<div class="mt-3">
							<BarChart
								data={[600, 500, 400, 300, 200]}
								categories={[
									'ideologi',
									'Politik',
									'Ekonomi',
									'Seni Budaya',
									'Pertahanan & Keamanan'
								]}
							/>
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
							<div class="d-flex ">
								<form action="" class="date-container">
									<input type="date" name="" id="" />
									<p>To</p>
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
									<td>1</td>
									<td>Binda DKI Jakarta</td>
									<td>234</td>
									<td>123</td>
									<td>124</td>
									<td>12</td>
								</tr>
								<tr>
									<td>1</td>
									<td>Binda DKI Jakarta</td>
									<td>234</td>
									<td>123</td>
									<td>124</td>
									<td>12</td>
								</tr>
								<tr>
									<td>1</td>
									<td>Binda DKI Jakarta</td>
									<td>234</td>
									<td>123</td>
									<td>124</td>
									<td>12</td>
								</tr>
								<tr>
									<td>1</td>
									<td>Binda DKI Jakarta</td>
									<td>234</td>
									<td>123</td>
									<td>124</td>
									<td>12</td>
								</tr>
								<tr>
									<td>1</td>
									<td>Binda DKI Jakarta</td>
									<td>234</td>
									<td>123</td>
									<td>124</td>
									<td>12</td>
								</tr>
								<tr>
									<td>1</td>
									<td>Binda DKI Jakarta</td>
									<td>234</td>
									<td>123</td>
									<td>124</td>
									<td>12</td>
								</tr>
								<tr>
									<td>1</td>
									<td>Binda DKI Jakarta</td>
									<td>234</td>
									<td>123</td>
									<td>124</td>
									<td>12</td>
								</tr>
							</tbody>
						</table>
					</div>
				</div>
			</div>
		</div>
	</div>
</div>

<style>
	.date-container {
		align-items: baseline;
		display: flex;
		gap: 1rem;
	}
	input[type='date'] {
		background: #23282e;
		border-right: none;
		border-left: none;
		color: #fbfdff;
	}
</style>
