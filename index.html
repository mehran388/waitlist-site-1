<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Company Visit Appointment</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f0f0f0;
      padding: 20px;
    }
    .container {
      max-width: 600px;
      background: #fff;
      padding: 20px;
      margin: auto;
      border-radius: 10px;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
    }
    h2, h3 {
      text-align: center;
    }
    input, textarea, button {
      width: 100%;
      padding: 10px;
      margin-top: 10px;
      margin-bottom: 20px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    button {
      background-color: #28a745;
      color: white;
      font-weight: bold;
      cursor: pointer;
    }
    button:hover {
      background-color: #218838;
    }
    .waitlist {
      margin-top: 30px;
    }
    .company {
      padding: 10px;
      background: #e9ecef;
      border-radius: 5px;
      margin-bottom: 10px;
      position: relative;
    }
    .action-buttons {
      position: absolute;
      top: 10px;
      right: 10px;
    }
    .action-buttons button {
      background-color: #007bff;
      margin-left: 5px;
    }
    .action-buttons button:hover {
      background-color: #0056b3;
    }
    .served {
      background-color: #d4edda;
    }
    #adminSection {
      display: none;
      margin-top: 20px;
    }
  </style>
</head>
<body>
  <div class="container">
    <h2>Company Visit Appointment</h2>
    <form id="bookingForm">
      <input type="text" id="companyName" placeholder="Company Name" required />
      <input type="text" id="contactPerson" placeholder="Contact Person" required />
      <input type="email" id="email" placeholder="Email" required />
      <textarea id="purpose" placeholder="Purpose of Visit" required></textarea>
      <button type="submit">Book Appointment</button>
    </form>

    <div class="waitlist">
      <h3>Waiting List</h3>
      <div id="waitListContainer"></div>
    </div>

    <div id="adminLogin">
      <input type="password" id="adminPassword" placeholder="Admin Password">
      <button onclick="loginAdmin()">Login as Admin</button>
    </div>

    <div id="adminSection">
      <button onclick="exportCSV()">Export to CSV</button>
    </div>
  </div>

  <script>
    const form = document.getElementById('bookingForm');
    const waitListContainer = document.getElementById('waitListContainer');
    const adminSection = document.getElementById('adminSection');
    const adminPassword = "admin123";

    let waitList = JSON.parse(localStorage.getItem('waitList')) || [];

    form.addEventListener('submit', function(e) {
      e.preventDefault();
      const company = {
        name: document.getElementById('companyName').value,
        contact: document.getElementById('contactPerson').value,
        email: document.getElementById('email').value,
        purpose: document.getElementById('purpose').value,
        time: new Date().toLocaleString(),
        served: false
      };
      waitList.push(company);
      saveList();
      renderList();
      form.reset();
    });

    function renderList() {
      waitListContainer.innerHTML = '';
      waitList.forEach((c, index) => {
        const div = document.createElement('div');
        div.className = 'company' + (c.served ? ' served' : '');
        div.innerHTML = `<strong>#${index + 1}</strong> - ${c.name} <br>
                         Contact: ${c.contact} | ${c.email} <br>
                         Purpose: ${c.purpose} <br>
                         Time: ${c.time}`;

        const actions = document.createElement('div');
        actions.className = 'action-buttons';
        if (!c.served) {
          const serveBtn = document.createElement('button');
          serveBtn.textContent = 'Mark Served';
          serveBtn.onclick = () => {
            c.served = true;
            saveList();
            renderList();
          };
          actions.appendChild(serveBtn);
        }
        const removeBtn = document.createElement('button');
        removeBtn.textContent = 'Remove';
        removeBtn.onclick = () => {
          waitList.splice(index, 1);
          saveList();
          renderList();
        };
        actions.appendChild(removeBtn);
        div.appendChild(actions);

        waitListContainer.appendChild(div);
      });
    }

    function saveList() {
      localStorage.setItem('waitList', JSON.stringify(waitList));
    }

    function loginAdmin() {
      const input = document.getElementById('adminPassword');
      if (input.value === adminPassword) {
        adminSection.style.display = 'block';
        input.disabled = true;
      } else {
        alert("Incorrect password.");
      }
    }

    function exportCSV() {
      let csvContent = "data:text/csv;charset=utf-8,";
      csvContent += "No,Company Name,Contact Person,Email,Purpose,Time,Served\n";
      waitList.forEach((c, i) => {
        const row = `${i + 1},${c.name},${c.contact},${c.email},${c.purpose},${c.time},${c.served ? 'Yes' : 'No'}`;
        csvContent += row + "\n";
      });
      const encodedUri = encodeURI(csvContent);
      const link = document.createElement("a");
      link.setAttribute("href", encodedUri);
      link.setAttribute("download", "appointment_waitlist.csv");
      document.body.appendChild(link);
      link.click();
      document.body.removeChild(link);
    }

    renderList();
  </script>
</body>
</html>
