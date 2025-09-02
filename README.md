# Srujan.io
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>BMSIT College Student Admission</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        body {font-family: Arial, sans-serif; background: #f7f7f9; margin: 0; padding: 0;}
        .container {
            max-width: 500px; 
            margin: 40px auto; 
            background: #fff; 
            padding: 32px 24px; 
            border-radius: 10px; 
            box-shadow: 0 2px 12px rgba(0,0,0,0.09);
        }
        h2 {text-align: center; color: #004080;}
        label {display: block; margin-top: 18px; margin-bottom: 6px; font-weight: 500;}
        input, select {width: 100%; padding: 8px; margin-bottom: 10px; font-size: 1em;}
        .docs-list {margin-top: 16px;}
        .docs-list label {font-weight: normal;}
        button {
            width: 100%; 
            padding: 12px; 
            background: #004080; 
            color: #fff; 
            border: none; 
            border-radius: 4px;
            font-size: 1.1em;
            cursor: pointer;
            margin-top: 20px;
        }
        button:hover {background: #002d5a;}
        .success {background: #e0ffe0; border: 1px solid #7af07a; padding: 18px; border-radius: 8px;}
    </style>
</head>
<body>
    <div class="container">
        <h2>BMSIT College Admission Form</h2>
        <form id="admissionForm">
            <label for="name">Full Name:</label>
            <input type="text" id="name" name="name" required>

            <label for="dob">Date of Birth:</label>
            <input type="date" id="dob" name="dob" required>

            <label for="email">Email Address:</label>
            <input type="email" id="email" name="email" required>

            <label for="course">Course Applying For:</label>
            <select id="course" name="course" required>
                <option value="">--Select Course--</option>
                <option value="B.E">B.E</option>
                <option value="M.Tech">M.Tech</option>
                <option value="PhD">PhD</option>
            </select>
            
            <div class="docs-list">
                <label>Please upload the following documents:</label>
                <label><input type="checkbox" name="docs" value="10th Marksheet" required> 10th Marksheet</label>
                <label><input type="checkbox" name="docs" value="12th Marksheet" required> 12th Marksheet</label>
                <label><input type="checkbox" name="docs" value="Transfer Certificate" required> Transfer Certificate</label>
                <label><input type="checkbox" name="docs" value="Caste Certificate"> Caste Certificate (if applicable)</label>
                <label><input type="checkbox" name="docs" value="Aadhar Card" required> Aadhar Card</label>
                <label><input type="checkbox" name="docs" value="Passport Size Photo" required> Passport Size Photo</label>
            </div>

            <label for="upload">Upload Documents (PDF/ZIP, max 10MB):</label>
            <input type="file" id="upload" name="upload" accept=".pdf,.zip" multiple required>
            
            <button type="submit">Submit Application</button>
        </form>
        <div id="successMessage" class="success" style="display:none;">
            <h3>Application Submitted!</h3>
            <p>Thank you for applying to BMSIT College. We will review your application and contact you soon.</p>
        </div>
    </div>
    <script>
        document.getElementById('admissionForm').onsubmit = function(e) {
            e.preventDefault();
            document.getElementById('admissionForm').style.display = 'none';
            document.getElementById('successMessage').style.display = 'block';
        }
    </script>
</body>
</html>
