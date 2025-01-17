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
        table {
            width: 100%;
            margin-bottom: 10px;
            border-collapse: collapse;
        }
        table td, table th {
            border: 1px solid #ddd;
            padding: 8px;
            text-align: center;
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
                <table>
                    <tr>
                        <th>Quiz 1</th>
                        <th>Quiz 2</th>
                        <th>Quiz 3</th>
                        <th>Quiz 4</th>
                        <th>Quiz 5</th>
                    </tr>
                    <tr>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                    </tr>
                </table>
            </div>
            <div class="subject" data-coefficient="7">
                <h2>Physics (Coefficient: 7)</h2>
                <table>
                    <tr>
                        <th>Quiz 1</th>
                        <th>Quiz 2</th>
                        <th>Quiz 3</th>
                        <th>Quiz 4</th>
                        <th>Quiz 5</th>
                    </tr>
                    <tr>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                    </tr>
                </table>
            </div>

            <!-- Additional subjects -->
            <div class="subject" data-coefficient="5">
                <h2>SVT (Coefficient: 5)</h2>
                <table>
                    <tr>
                        <th>Quiz 1</th>
                        <th>Quiz 2</th>
                        <th>Quiz 3</th>
                        <th>Quiz 4</th>
                        <th>Quiz 5</th>
                    </tr>
                    <tr>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                    </tr>
                </table>
            </div>
            <div class="subject" data-coefficient="4">
                <h2>French (Coefficient: 4)</h2>
                <table>
                    <tr>
                        <th>Quiz 1</th>
                        <th>Quiz 2</th>
                        <th>Quiz 3</th>
                        <th>Quiz 4</th>
                        <th>Quiz 5</th>
                    </tr>
                    <tr>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                    </tr>
                </table>
            </div>
            <div class="subject" data-coefficient="4">
                <h2>Sports (Coefficient: 4)</h2>
                <table>
                    <tr>
                        <th>Quiz 1</th>
                        <th>Quiz 2</th>
                        <th>Quiz 3</th>
                        <th>Quiz 4</th>
                        <th>Quiz 5</th>
                    </tr>
                    <tr>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                    </tr>
                </table>
            </div>
            <div class="subject" data-coefficient="2">
                <h2>Philosophy (Coefficient: 2)</h2>
                <table>
                    <tr>
                        <th>Quiz 1</th>
                        <th>Quiz 2</th>
                        <th>Quiz 3</th>
                        <th>Quiz 4</th>
                        <th>Quiz 5</th>
                    </tr>
                    <tr>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                    </tr>
                </table>
            </div>
            <div class="subject" data-coefficient="2">
                <h2>English (Coefficient: 2)</h2>
                <table>
                    <tr>
                        <th>Quiz 1</th>
                        <th>Quiz 2</th>
                        <th>Quiz 3</th>
                        <th>Quiz 4</th>
                        <th>Quiz 5</th>
                    </tr>
                    <tr>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                    </tr>
                </table>
            </div>
            <div class="subject" data-coefficient="2">
                <h2>Arabic (Coefficient: 2)</h2>
                <table>
                    <tr>
                        <th>Quiz 1</th>
                        <th>Quiz 2</th>
                        <th>Quiz 3</th>
                        <th>Quiz 4</th>
                        <th>Quiz 5</th>
                    </tr>
                    <tr>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                    </tr>
                </table>
            </div>
            <div class="subject" data-coefficient="2">
                <h2>Islamic Education (Coefficient: 2)</h2>
                <table>
                    <tr>
                        <th>Quiz 1</th>
                        <th>Quiz 2</th>
                        <th>Quiz 3</th>
                        <th>Quiz 4</th>
                        <th>Quiz 5</th>
                    </tr>
                    <tr>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                    </tr>
                </table>
            </div>
            <div class="subject" data-coefficient="2">
                <h2>Discipline (Coefficient: 2)</h2>
                <table>
                    <tr>
                        <th>Quiz 1</th>
                        <th>Quiz 2</th>
                        <th>Quiz 3</th>
                        <th>Quiz 4</th>
                        <th>Quiz 5</th>
                    </tr>
                    <tr>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                        <td><input type="text" class="quiz" placeholder="Grade"></td>
                    </tr>
                </table>
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
                    const quizzes = subject.querySelectorAll('.quiz');
                    const grades = Array.from(quizzes).map(input => parseFloat(input.value.trim()));
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
