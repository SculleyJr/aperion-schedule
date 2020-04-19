<script>
	 let name = "Sean Sculley";
	 let points = 100;

	 function Employee(employeeId, firstName, lastName, dob, position, team) {
		 this.employeeId = '';
		 this.firstName = '';
		 this.lastName = '';
		 this.dob = new Date(dob);
		 this.position = '';
		 this.team = '';
	 }

	 function addNewEmployee(employeeId, firstName, lastName, dob, position, team) {
		 var newEmployee = Object.create(Employee);
		 employeeId = newEmployee.employeeId; 
		 firstName = newEmployee.firstName;
		 this.lastName = newEmployee.lastName;
		 dob = newEmployee.dob;
		 position = newEmployee.position;
		 team = newEmployee.team;

	 }

	 

	 const addPoint = () => points += 1;
	 const removePoint = () => points -= 1;

	 var leads = [];
	 console.log(Employee);

</script>

<main>
<div class="container">
	<div class="card">
		<h1>Hello {name}!</h1>
		<h3>{points}</h3>
		<button class="btn"on:click={addPoint}>+1</button>
		<button class="btn btn-dark"on:click={removePoint}>-1</button>

		<form id="newEmployee" action="/action_page.php">
			Employee ID: <input type="text" name="employeeId"><br>
  			First name: <input type="text" name="firstName"><br>
  			Last name: <input type="text" name="lastName"><br>
			Date of Birth: <input type="text" name="dob"><br>
			Position: <input type="text" name="position"><br>
			Team number: <input type="text" name="team"><br>
  <input type="button" onclick="addNewEmployee()" value="Submit">
</form>
	</div>
</div>
	

</main>

<style>
h1{
	color: #204f6e;
}
</style>