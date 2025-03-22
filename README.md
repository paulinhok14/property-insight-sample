# 🏠 Property Insight
### **Smart Insights for Smarter Investments**
### 🎯 Your AI-Smart Radar for Real Estate Opportunities

###### MVP

Property Insight is an app that helps you identify amazing real estate opportunities, track market trends, and manage your property investments visually — built using Python, Streamlit, Folium, AI and many other [cool technologies](#️-technologies-used).

## 🎬 See it in Action!

[![mvp_functioning](docs/1_first_app_mvp.png)](https://github.com/user-attachments/assets/3ee9ddfd-5a2f-4945-9576-56fa669c6ed5)


### Try it here: [🔗 Property Insight](https://sjc-housing-prices.onrender.com/)

### 🔥 Motivation
Finding the perfect real estate opportunity can be daunting, but staying informed is crucial. That's why I created Property Insight — a tool designed to help you spot the best deals in the market.

I realized that traditional methods just don't cut it when it comes to identifying valuable properties. I wanted an easy way to find good deals without relying on a broker. That's where Property Insight comes in.

With this app, I can clearly visualize market disfunctions, property prices, and potential deals in a beautifully organized way. Plus, I can use an AI model to predict fair prices, giving me a clear advantage in the market.

I’ve created this while searching for my first own house (so it started with a personal purpose), and it was a game-changer! I believe it can add value to other real estate enthusiasts too.

# 🚧 Current Status: **Under development**

## 🎯 Key Features:

### ✅ Completed
* [x] WebScrap a significant amount of property data on SJC region
* [x] Add geospatial (lat/long) data in order to plot property marks on a Map
* [x] Preprocess and Feature Engineer property data
* [x] Create and train a House Price Predictor model based on property features
* [x] Deploy AI Price Predictor model in a REST API
* [x] Create a Streamlit web app with a interactive Map provider
* [x] Add an images carrousell component to show real pictures from selected property
* [x] Embed the Estimated Fair Value and the Premium/Discount compared to published Price metrics on properties panel
* [x] Create Dockerfile
* [x] Automatic tests using GitHub Actions
* [x] Deploy on Render
* [x] Add Pages and Navigation system to accomodate new features structure
* [x] Create a Property Price Predictor feature page that takes input, request to model API and return a Estimated Fair Price
* [x] Deploy on AWS (EC2, Lambda)
* [x] Create a logo and an app name with commercial appeal
* [x] Add logo to Sidebar top

### 📝 To Do

* [ ] Add functional filters, such as: Type, Neighborhood, Price Range, Premium/Discount threshold, etc.
* [ ] Adjust Folium pop-up with key information, such as current Price, Estimated Price, Premium/Discount. 
* [ ] Create a page with a Line Items table
* [ ] Create authentication process/profiling

## 🚀 How to Run it?

To run **Property Insight**, you’ll need the following:

- A working installation of **[Python](https://www.python.org/)**.


Then, you can run the following commands on your terminal:

```bash
# Install Dependencies:
pip install -r requirements.txt 

# Build Docker image:
docker build -t housing-prices-monitor .

# Start Price Predictor Model API:
cd .\api\
uvicorn app_price_predictions:app --reload

# Run application:
streamlit run .\app.py

# Or you can do both just by calling start_services.sh:
chmod +x start_services.sh
./start_services.sh

# The application will be available at http://localhost:8501.

# Price Predictor Model API will be available at http://localhost:8000.
```

## 🛠️ Technologies Used

<table style="width:100%">
  <tr>
    <th>Category</th>
    <th>Technology</th>
  </tr>
  <tr>
    <td>📦 Programming Language</td>
    <td><a href="https://www.python.org/">Python</a></td>
  </tr>
  <tr>
    <td>⛏️ Data Scrapping</td>
    <td><a href="https://www.selenium.dev/">Selenium</a>,  <a href="https://pandas.pydata.org/">Pandas</a></td></td>
  </tr>
  <tr>
    <td>🤖 AI</td>
    <td><a href="https://scikit-learn.org/stable/"/>Scikit-Learn</a>, <a href="https://pytorch.org/">Pytorch</a></td>
  </tr>  
  <tr>
  <tr>
    <td>🌐 Web Framework</td>
    <td><a href="https://streamlit.io/">Streamlit</a></td>
  </tr>  
  <tr>
    <td>🖼️ Maps & Navigation</td>
    <td><a href="https://pypi.org/project/folium/">Folium</a>
  </tr>
  <tr>
    <td>🌍 Maps API</td>
    <td><a href="https://www.openstreetmap.org/">OpenStreetMap</a></td>
  </tr>
    <tr>
    <td>🐳 Containerization</td>
    <td><a href="https://www.docker.com/">Docker</a></td>
  </tr>
  <tr>
    <td>🚀 Model Deployment</td>
    <td><a href="https://fastapi.tiangolo.com/">FastAPI</a></td>
  </tr>
  <tr>
    <td>🚀 App Deployment</td>
    <td><a href="https://sjc-housing-prices.onrender.com/">Render</a>, <a href="https://aws.amazon.com/">AWS EC2</a></td>
  </tr>
  <tr>
    <td>💻 Testing</td>
    <td><a href="https://docs.pytest.org/en/stable"/>Pytest</a>, <a href="https://github.com/features/actions">GitHub Actions</a></td>
  </tr>
  <tr>
    <td>🔧 Code Formatting</td>
    <td><a href="https://www.pylint.org/">Pylint</a></td>
  </tr>
</table>
