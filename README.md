<h1>Collaborative Development of a Full-Stack Application: Group 6</h1>

<h2>Project Description</h2>
<p>This project is a full-stack web application designed to provide user authentication, role-based access control, profile management, and email verification. It consists of:</p>
<ul>
  <li><strong>Backend:</strong> Node.js + MySQL API</li>
  <li><strong>Frontend:</strong> Angular 19</li>
  <li><strong>Testing:</strong> Fake backend for initial testing, real API for integration.</li>
</ul>
<p>The application allows users to register, log in, and manage their profiles securely with authentication and role-based access control.</p>

<hr>

<h2>Setup Instructions</h2>

<h3>Prerequisites</h3>
<p>Before setting up the project, ensure you have the following installed:</p>
<ul>
  <li><strong>Node.js</strong> (v16+)</li>
  <li><strong>MySQL</strong> (Latest Version)</li>
  <li><strong>Angular CLI</strong> (v19+)</li>
  <li><strong>Git</strong> (Latest Version)</li>
</ul>

<h3>Backend Setup (Node.js + MySQL)</h3>
<ol>
  <li><strong>Clone the repository:</strong>
    <pre><code>git clone https://github.com/yourusername/groupX-fullstack-app.git
cd backend</code></pre>
  </li>
  <li><strong>Install dependencies:</strong>
    <pre><code>npm install</code></pre>
  </li>
  <li><strong>Configure the environment variables:</strong>
    <pre><code>DB_HOST=localhost
DB_USER=root
DB_PASS=yourpassword
JWT_SECRET=your_secret_key
SMTP_HOST=smtp.mailtrap.io
SMTP_USER=your_username
SMTP_PASS=your_password</code></pre>
  </li>
  <li><strong>Run the database migrations:</strong>
    <pre><code>npm run migrate</code></pre>
  </li>
  <li><strong>Start the backend server:</strong>
    <pre><code>npm start</code></pre>
  </li>
</ol>



<hr>

<h2>API Endpoints</h2>
<table class="api-table">
  <tr>
    <th>Method</th>
    <th>Endpoint</th>
    <th>Description</th>
    <th>Auth Required</th>
  </tr>
  <tr>
    <td class="api-method">POST</td>
    <td>/accounts/register</td>
    <td>Register a new user</td>
    <td class="auth-no">NO</td>
  </tr>
  <tr>
    <td class="api-method">POST</td>
    <td>/accounts/refresh-token</td>
    <td>The refresh token is sent and returned via cookies.</td>
    <td class="auth-no">NO</td>
  </tr>
  <tr>
    <td class="api-method">POST</td>
    <td>/accounts/revoke-token</td>
    <td>Admin users can revoke the tokens of any account, regular users can only revoke their own tokens.</td>
    <td class="auth-yes">YES</td>
  </tr>
  <tr>
    <td class="api-method">POST</td>
    <td>/accounts/authenticate</td>
    <td>Accounts must be verified before authenticating.</td>
    <td class="auth-no">NO</td>
  </tr>
  <tr>
    <td class="api-method">POST</td>
    <td>/accounts/verify-email</td>
    <td>Verify a new account with a verification token received by email after registration.</td>
    <td class="auth-no">NO</td>
  </tr>
  <tr>
    <td class="api-method">POST</td>
    <td>/accounts/forgot-password</td>
    <td>Submit email address to reset the password on an account.</td>
    <td class="auth-no">NO</td>
  </tr>
  <tr>
    <td class="api-method">POST</td>
    <td>/accounts/validate-reset-token</td>
    <td>Validate the reset password token received by email.</td>
    <td class="auth-no">NO</td>
  </tr>
  <tr>
    <td class="api-method">POST</td>
    <td>/accounts/reset-password</td>
    <td>Reset the password for an account.</td>
    <td class="auth-no">NO</td>
  </tr>
  <tr>
    <td class="api-method">GET</td>
    <td>/accounts</td>
    <td>Get a list of all accounts.</td>
    <td class="auth-yes">YES</td>
  </tr>
  <tr>
    <td class="api-method">GET</td>
    <td>/accounts/:id</td>
    <td>Get a single account by ID.</td>
    <td class="auth-yes">YES</td>
  </tr>
  <tr>
    <td class="api-method">PUT</td>
    <td>/accounts/:id</td>
    <td>Update an account.</td>
    <td class="auth-yes">YES</td>
  </tr>
  <tr>
    <td class="api-method">DELETE</td>
    <td>/accounts/:id</td>
    <td>Delete an account.</td>
    <td class="auth-yes">YES</td>
  </tr>
</table>
<hr>


<hr>

<h2>Testing Instructions</h2>

<h3>Backend Testing (Postman)</h3>
<ol>
  <li><strong>Install <a href="https://www.postman.com/">Postman</a>.</strong></li>
  <li><strong>Import <code>postman_collection.json</code> into Postman.</strong></li>
  <li><strong>Run API requests</strong> for login, register, and user management.</li>
</ol>


<hr>

<h2>Contributors</h2>
<table border="1">
  <tr>
    <th>Name</th>
    <th>Role</th>
  </tr>
  <tr>
    <td>Lourd Angelo Bufete</td>
    <td>Backend Developer</td>
  </tr>
  <tr>
    <td>Romy A. Formentera Jr.</td>
    <td>Frontend Developer</td>
  </tr>
  <tr>
    <td>Roy P. Estorco</td>
    <td>Tester &</td>
  </tr>
  <tr>
    <td>Raquel Pacure</td>
    <td>Documentation Specialist</td>
  </tr>
  <tr>
    <td>Ly Ann Kate Candido</td>
    <td>Documentation Specialist</td>
<tr>
<td>Jade Steve Molejon</td>
    <td>DevOps Lead</td>
</tr>
  </tr>
</table>