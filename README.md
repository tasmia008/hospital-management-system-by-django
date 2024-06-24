# hospital management system by django
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Hospital Management System</title>
</head>
<body>

<h1>Hospital Management System</h1>

<h2>Features</h2>

<h3>Admin</h3>
<ul>
  <li>Signup their account. Then Login (No approval Required).</li>
  <li>Can register/view/approve/reject/delete doctor (approve those doctor who applied for job in their hospital).</li>
  <li>Can admit/view/approve/reject/discharge patient (discharge patient when treatment is done).</li>
  <li>Can Generate/Download Invoice pdf (Generate Invoice according to medicine cost, room charge, doctor charge and other charge).</li>
  <li>Can view/book/approve Appointment (approve those appointments which is requested by patient).</li>
</ul>

<h3>Doctor</h3>
<ul>
  <li>Apply for job in hospital. Then Login (Approval required by hospital admin, Then only doctor can login).</li>
  <li>Can only view their patient details (symptoms, name, mobile ) assigned to that doctor by admin.</li>
  <li>Can view their discharged(by admin) patient list.</li>
  <li>Can view their Appointments, booked by admin.</li>
  <li>Can delete their Appointment, when doctor attended their appointment.</li>
</ul>

<h3>Patient</h3>
<ul>
  <li>Create account for admit in hospital. Then Login (Approval required by hospital admin, Then only patient can login).</li>
  <li>Can view assigned doctor's details like ( specialization, mobile, address).</li>
  <li>Can view their booked appointment status (pending/confirmed by admin).</li>
  <li>Can book appointments.(approval required by admin)</li>
  <li>Can view/download Invoice pdf (Only when that patient is discharged by admin).</li>
</ul>

<h2>How to Run This Project</h2>
<ol>
  <li>Install Python(3.7.6) (Don't Forget to Tick Add to Path while installing Python).</li>
  <li>Open Terminal and Execute Following Commands:
    <ul>
      <li><code>pip install django==3.0.5</code></li>
      <li><code>pip install django-widget-tweaks</code></li>
      <li><code>pip install xhtml2pdf</code></li>
    </ul>
  </li>
  <li>Download This Project Zip Folder and Extract it.</li>
  <li>Move to project folder in Terminal. Then run following Commands:
    <ul>
      <li><code>py manage.py makemigrations</code></li>
      <li><code>py manage.py migrate</code></li>
      <li><code>py manage.py runserver</code></li>
    </ul>
  </li>
  <li>Now enter following URL in Your Browser Installed On Your PC:
    <ul>
      <li><code>http://127.0.0.1:8000/</code></li>
    </ul>
  </li>
</ol>

<h2>Changes Required for Contact Us Page</h2>
<ol>
  <li>In <code>settings.py</code> file, You have to give your email and password:
    <ul>
      <li><code>EMAIL_HOST_USER = 'youremail@gmail.com'</code></li>
      <li><code>EMAIL_HOST_PASSWORD = 'your email password'</code></li>
      <li><code>EMAIL_RECEIVING_USER = 'youremail@gmail.com'</code></li>
    </ul>
  </li>
  <li>Login to Gmail through host email id in your browser and open following link and turn it ON:
    <ul>
      <li><a href="https://myaccount.google.com/lesssecureapps">https://myaccount.google.com/lesssecureapps</a></li>
    </ul>
  </li>
</ol>

<h2>Drawbacks/LoopHoles</h2>
<ul>
  <li>Any one can be Admin. There is no Approval required for admin account. So you can disable admin signup process and use any logic like creating superuser.</li>
  <li>There should be at least one doctor in hospital before admitting patient. So first add doctor.</li>
  <li>On update page of doctor/patient you must have to update password.</li>
</ul>

</body>
</html>

