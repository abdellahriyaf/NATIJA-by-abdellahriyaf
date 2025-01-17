<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fixed Subjects Semester Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            margin: 0;
            padding: 20px;
            text-align: center;
        }
        .container {
            max-width: 700px;
            margin: 0 auto;
            background: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
        }
        h1 {
            color: #333;
            margin-bottom: 20px;
        }
        .subject {
            border: 1px solid #ddd;
            padding: 10px;
            margin-bottom: 10px;
            border-radius: 5px;
            text-align: left;
        }
        .subject h2 {
            margin: 0;
            font-size: 16px;
            margin-bottom: 10px;
        }
        .input-row {
            display: flex;
            justify-content: space-between;
            margin-bottom: 10px;
        }
        input[type="text"] {
            width: 80%;
            padding: 8px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        button {
            background-color: #007BFF;
            color: #fff;
            border: none;
            padding: 10px 20px;
            font-size: 16px;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 10px;
        }
        button:hover {
            background-color: #0056b3;
        }
        .result {
            margin-top: 20px;
            font-size: 18px;
            color: #28a745;
        }
        .error {
            color: #dc3545;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Semester Average Calculator</h1>
        <div id="subjects-container">
            <!-- Subjects with predefined coefficients -->
            <div class="subject" data-coefficient="7">
                <h2>Math (Coefficient: 7)</h2>
                <div class="input-row">
                    <label for="math">Enter Grades (up to 5 quizzes):</label>
                </div>
                <input type="text" class="grades" placeholder="Comma-separated grades (e.g., 14, 15, 16)">
            </div>
            <div class="subject" data-coefficient="7">
                <h2>Physics (Coefficient: 7)</h2>
                <div class="input-row">
                    <label for="physics">Enter Grades (up to 5 quizzes):</label>
                </div>
                <input type="text" class="grades" placeholder="Comma-separated grades (e.g., 12, 14, 16)">
            </div>
            <div class="subject" data-coefficient="5">
                <h2>SVT (Coefficient: 5)</h2>
                <div class="input-row">
                    <label for="svt">Enter Grades (up to 5 quizzes):</label>
                </div>
                <input type="text" class="grades" placeholder="Comma-separated grades (e.g., 13, 14, 15)">
            </div>
            <div class="subject" data-coefficient="4">
                <h2>Sports (Coefficient: 4)</h2>
                <div class="input-row">
                    <label for="sports">Enter Grades (up to 5 quizzes):</label>
                </div>
                <input type="text" class="grades" placeholder="Comma-separated grades (e.g., 18, 19, 20)">
            </div>
            <div class="subject" data-coefficient="4">
                <h2>French (Coefficient: 4)</h2>
                <div class="input-row">
                    <label for="french">Enter Grades (up to 5 quizzes):</label>
                </div>
                <input type="text" class="grades" placeholder="Comma-separated grades (e.g., 14, 15)">
            </div>
            <div class="subject" data-coefficient="2">
                <h2>Philosophy (Coefficient: 2)</h2>
                <div class="input-row">
                    <label for="philosophy">Enter Grades (up to 5 quizzes):</label>
                </div>
                <input type="text" class="grades" placeholder="Comma-separated grades (e.g., 12, 14)">
            </div>
            <div class="subject" data-coefficient="2">
                <h2>Islamic Education (Coefficient: 2)</h2>
                <div class="input-row">
                    <label for="islamic-education">Enter Grades (up to 5 quizzes):</label>
                </div>
                <input type="text" class="grades" placeholder="Comma-separated grades (e.g., 17, 18)">
            </div>
            <div class="subject" data-coefficient="2">
                <h2>English (Coefficient: 2)</h2>
                <div class="input-row">
                    <label for="english">Enter Grades (up to 5 quizzes):</label>
                </div>
                <input type="text" class="grades" placeholder="Comma-separated grades (e.g., 15, 16)">
            </div>
            <div class="subject" data-coefficient="2">
                <h2>Arabic (Coefficient: 2)</h2>
                <div class="input-row">
                    <label for="arabic">Enter Grades (up to 5 quizzes):</label>
                </div>
                <input type="text" class="grades" placeholder="Comma-separated grades (e.g., 13, 14)">
            </div>
            <div class="subject" data-coefficient="1">
                <h2>perseverance (Coefficient: 1)</h2>
                <div class="input-row">
                    <label for="perseverance">Enter Grades (up to 5 quizzes):</label>
                </div>
                <input type="text" class="grades" placeholder="Comma-separated grades (e.g., 14, 15)">
            </div>
        </div>
        <button onclick="calculateSemesterAverage()">Calculate Semester Average</button>
        <div id="result" class="result"></div>
    </div>

    <script>
        function calculateSemesterAverage() {
            const subjects = document.querySelectorAll('.subject');
            const resultDiv = document.getElementById('result');

            let totalWeighted = 0;
            let totalCoefficients = 0;

            try {
                subjects.forEach(subject => {
                    const gradesInput = subject.querySelector('.grades').value;
                    const grades = gradesInput.split(',').map(g => parseFloat(g.trim()));
                    const coefficient = parseFloat(subject.dataset.coefficient);

                    // Filter out invalid grades
                    const validGrades = grades.filter(g => !isNaN(g));
                    if (validGrades.length === 0) {
                        throw new Error('All subjects must have at least one valid grade.');
                    }

                    // Calculate subject average
                    const subjectAverage = validGrades.reduce((a, b) => a + b, 0) / validGrades.length;

                    totalWeighted += subjectAverage * coefficient;
                    totalCoefficients += coefficient;
                });

                if (totalCoefficients === 0) {
                    throw new Error('Total coefficient cannot be zero.');
                }

                const semesterAverage = totalWeighted / totalCoefficients;
                resultDiv.innerHTML = `Semester Average: <strong>${semesterAverage.toFixed(2)}</strong>`;
                resultDiv.className = 'result';
            } catch (error) {
                resultDiv.innerHTML = `Error: ${error.message}`;
                resultDiv.className = 'error';
            }
        }
    </script>
</body>
</html>
