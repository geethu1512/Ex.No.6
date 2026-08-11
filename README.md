# Ex.No.6 Development of Python Code Compatible with Multiple AI Tools

# Date: 11-08-26
# Register no. : 212224040089
# Aim: Write and implement Python code that integrates with multiple AI tools to automate the task of interacting with APIs, comparing outputs, and generating actionable insights with Multiple AI Tools

#AI Tools Required:

# Explanation:
Experiment the persona pattern as a programmer for any specific applications related with your interesting area. 
Generate the outoput using more than one AI tool and based on the code generation analyse and discussing that. 
PROMPT DESIGN AND EXECUTION
Stage 1: Prompt for Generating Python Code to Interact with Multiple APIs
Designed Prompt

Act as a professional Python developer. Write Python code that fetches machine performance data from two REST APIs, parses the JSON responses, and extracts important metrics such as temperature, vibration, and machine status. Include proper error handling, functions, and comments to make the code easy to understand.

AI-Generated Response – Sample Code
~~~
import requests

def fetch_api_data(url):
    try:
        response = requests.get(url, timeout=10)
        response.raise_for_status()
        return response.json()
    except requests.exceptions.RequestException as e:
        print("Error fetching data:", e)
        return None

api1_url = "https://api1.example.com/machine"
api2_url = "https://api2.example.com/machine"

data1 = fetch_api_data(api1_url)
data2 = fetch_api_data(api2_url)

if data1:
    print("API 1 Data:", data1)

if data2:
    print("API 2 Data:", data2)
~~~
Output

The Python program successfully demonstrates how to:

Connect to REST APIs.
Send HTTP requests.
Receive JSON data.
Handle API connection errors.
Display machine monitoring data.
Reuse the same function for multiple APIs.
Stage 2: Prompt for Comparing Outputs
Designed Prompt

Compare the outputs received from API 1 and API 2. Calculate the differences in temperature and vibration levels and check whether the machine status values match. Display the comparison results clearly.

AI-Generated Response – Comparison Code
~~~
def compare_data(d1, d2):
    comparison = {
        "temperature_difference":
            d1["temperature"] - d2["temperature"],

        "vibration_difference":
            d1["vibration"] - d2["vibration"],

        "status_match":
            d1["status"] == d2["status"]
    }

    return comparison


if data1 and data2:
    result = compare_data(data1, data2)
    print("Comparison Result:", result)
~~~
Output

The program compares the machine data obtained from both APIs and provides:

Temperature difference.
Vibration difference.
Machine status comparison.
A clear indication of whether both API results match.
Stage 3: Prompt for Generating Actionable Insights
Designed Prompt

Based on the comparison results, generate actionable maintenance recommendations. Display a warning when temperature variation is greater than 10°C, generate an alert when vibration variation is greater than 5 units, and recommend inspection when the machine status differs between the two APIs.

AI-Generated Response – Insight Code
~~~
def generate_insights(comparison):

    if abs(comparison["temperature_difference"]) > 10:
        print("Warning: Significant temperature variation detected.")

    if abs(comparison["vibration_difference"]) > 5:
        print("Alert: Vibration levels require inspection.")

    if not comparison["status_match"]:
        print("Machine status mismatch detected.")
        print("Recommendation: Perform immediate machine inspection.")


if data1 and data2:
    comparison = compare_data(data1, data2)
    generate_insights(comparison)
~~~
Output

The program generates maintenance alerts based on the comparison results.

For example:

Temperature variation detected → Check the machine cooling system.
High vibration detected → Inspect bearings and moving components.
Status mismatch → Verify machine condition immediately.
Normal values → Continue regular monitoring.
Analysis of Multiple AI Tools
Criteria	ChatGPT	Gemini	Claude
Code Structure	Well structured	Simple and functional	Detailed and structured
Error Handling	Good	Basic	Good
Code Comments	Clear	Limited	Detailed
Modularity	High	Moderate	High
Practical Relevance	High	Moderate	High
Ease of Understanding	High	High	High
Overall Output	Balanced	Concise	Detailed
Observations
ChatGPT generated well-structured and easy-to-understand Python code with good error handling.
Gemini generated simpler code that was functional and easy to implement.
Claude provided detailed code with additional explanations and good modularity.
All three AI tools were able to understand the programmer persona and generate relevant Python code.
Structured prompts resulted in better-organized outputs.
Adding error-handling requirements improved the reliability of the generated code.
Breaking the task into different stages made the code easier to develop and test.
Prompt refinement improved the quality and practical usefulness of the generated solutions.
Comparison of Generated Code
ChatGPT

Provided a balanced solution with:

Clear functions
Proper error handling
Simple syntax
Good code organization
Practical implementation
Gemini

Provided:

Simple implementation
Shorter code
Basic error handling
Easy-to-understand structure
Claude

Provided:

Detailed implementation
Strong modular structure
More explanations
Additional considerations for improving the application
Reflection Note

The experiment demonstrates that prompt clarity directly influences AI-generated code quality. When the prompts included a specific role, clear requirements, and expected outputs, the AI tools generated more useful and organized Python programs.

The following prompt engineering techniques were particularly useful:

Persona Pattern: “Act as a professional Python developer.”
Clear task description
Step-by-step task breakdown
Specific output requirements
Error-handling instructions
Threshold-based conditions
Request for modular and reusable functions

The experiment also showed that different AI tools may produce different coding styles even when the same prompt is used.

Future Improvements

The application can be improved by:

Adding API authentication using API keys or tokens.
Using actual machine monitoring APIs instead of sample URLs.
Defining safe temperature and vibration thresholds based on machine specifications.
Adding data visualization using Python libraries.
Storing machine data in a database.
Adding unit test cases to verify the generated functions.
Using logging instead of only print() statements.
Adding automatic alerts for critical machine conditions.
Creating a dashboard to display real-time machine status.
Using historical data to improve predictive maintenance.
# Conclusion

The experiment successfully demonstrated the use of multiple AI tools for Python code generation in a smart manufacturing application. ChatGPT, Gemini, and Claude were used to generate and analyze Python code for API interaction, data comparison, and maintenance recommendations.

The comparison showed that structured and role-based prompts significantly improve AI-assisted coding performance. Different AI tools provided different levels of detail, structure, and explanation, but all were able to generate useful solutions when the requirements were clearly specified.

Therefore, effective prompt engineering can improve the accuracy, modularity, readability, and practical usefulness of AI-generated Python code.

# Result

The corresponding prompt was executed successfully using multiple AI tools, and the generated Python code was compared and analyzed for structure, error handling, clarity, and practical relevance.


