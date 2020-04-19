<script>

function Employee(employeeId, firstName, lastName, dob, position, team) {
		 this.employeeId = employeeId;
		 this.firstName = firstName;
		 this.lastName = lastName;
		 this.dob = new Date(dob);
		 this.position = position;
		 this.team = team;
	 }

function UI() {}

UI.prototype.addEmployeeToList = function(employee){
	const list = document.getElementById('employee-list');
	//Create table row element for employee list
	const row =  document.createElement('tr');

	row.innerHTML= `
	<td>${employee.employeeId}</td>
	<td>${employee.firstName}</td>
	<td>${employee.lastName}</td>
	<td>${employee.dob}</td>
	<td>${employee.position}</td>
	<td>${employee.team}</td>
	<td><a href="#" class="delete">X</a></td>
	`;
	list.appendChild(row);


	console.log(row);
}


window.onload=function(){
	 document.getElementById('newEmployee').addEventListener('submit', 
	 function(e){
			 const employeeId = document.getElementById('employeeId').value,
					firstName = document.getElementById('firstName').value,
					lastName = document.getElementById('lastName').value,
					dob = document.getElementById('dob').value,
					position = document.getElementById('position').value,
					team = document.getElementById('team').value

					
					
					const employee =  new Employee(employeeId, firstName, lastName, dob, position, team);

					const ui = new UI();

					console.log(ui);

					ui.addEmployeeToList(employee);


					

					
					
					
					
		 e.preventDefault();
	 });

}
		


	 

	 

	

	 


	 



</script>

<main>
<div class="container">
	<div class="card">

		<form id="newEmployee" >
			Employee ID: <input type="text" id="employeeId" ><br>
  			First name: <input type="text" id="firstName" ><br>
  			Last name: <input type="text" id="lastName" ><br>
			Date of Birth: <input type="text" id="dob" ><br>
			Position: <input type="text" id="position" ><br>
			Team number: <input type="text" id="team" ><br>
  <input  type="submit"  value="Submit">
</form>
	</div>
</div>

<table class="ui-table">
      <thead>
        <tr>
          <th>ID</th>
          <th>Name</th>
          <th>Last Name</th>
          <th>DOB</th>
          <th>Position</th>
          <th>Team Number</th>
          <th></th>
        </tr>
      </thead>
      <tbody id="employee-list"></tbody>
    </table>
	

</main>

<style>
h1{
	color: #204f6e;
}

.ui-table{
	margin: 10%;
}

.ui-table > tr {
	align-content: center;
}
</style>