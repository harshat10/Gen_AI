### TEAM NAME : CODE JOINTERS 
## Personalized Career and Skills Advisor
# CAREER AI
### PROBLEM STATEMENT : 
This is Harshat. From code jointers team. Many students and professionals are unclear on their career path due to an absence of customized direction, undefined skills-to-job mapping, and disparate menus of resources. In addition, most career counseling service is general and generally isn't accessible.
### SOLUTION :
Career AI acts as an intelligent assistant and provides personalized employment guidance by analyzing a user's abilities, interests, education, and personal goals. It will provide recommendations for potential career options, suggested learning paths, and suggested skill-building resources based on the user.
### CORE FEATURES :
#### 1.Profile Evaluation
Users provide their skills, education, and career interests.
#### 2.Career Recommender
AI provides recommendations for potential career roles (e.g., Data Scientist, UI/UX Designer, Business Analyst).
#### 3.Skill Gap Analyzer
Explores incompleteness of skills, and how to fill those gaps.
#### 4.Learning Pathway 
Curates courses, certifications and projects from online destiinations.
#### 5.Job Market Insights
Real-time trends for in-demand skills, salaries and opportunities.
#### 6.Interactive Chatbot 
Users can ask questions related to their career questions and gain further guidance.
### career_advisor.py:
```
<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap');

/* Apply Montserrat font globally */
* {
    font-family: 'Montserrat', sans-serif;
}

/* Title style */
.css-10trblm { 
    font-family: 'Montserrat', sans-serif;
    font-size: 32px !important;
    color: #2E86C1;
    font-weight: 700;
}

/* Sidebar style */
.css-1d391kg {
    font-family: 'Montserrat', sans-serif;
    font-size: 16px;
}
</style>
import streamlit as st
career_data = {
    "Data Science": {
        "skills": ["Python", "Statistics", "Machine Learning", "SQL", "Visualization"],
        "certifications": ["Coursera Data Science", "Google Data Analytics", "AWS ML Specialty"],
        "workshops": ["Kaggle competitions", "AI/ML hackathons", "TensorFlow workshops"]
    },
    "Web Development": {
        "skills": ["HTML", "CSS", "JavaScript", "React", "Node.js", "Databases"],
        "certifications": ["Meta Frontend Developer", "Full-Stack Open", "Google Cloud Web Specialist"],
        "workshops": ["Web Dev Bootcamps", "Open source hackathons", "JS meetups"]
    },
    "Music Production": {
        "skills": ["DAWs (FL Studio, Logic Pro)", "Sound Design", "Mixing & Mastering", "Music Theory"],
        "certifications": ["Berklee Online Music Production", "Ableton Live Certified Training"],
        "workshops": ["Music hackathons", "Recording workshops", "Beat-making sessions"]
    }
}
def generate_timetable(skills, hours_per_day=2):
    timetable = {}
    days = ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday", "Sunday"]
    for i, skill in enumerate(skills):
        timetable[days[i % 7]] = f"📖 Study {skill} for {hours_per_day} hours"
    return timetable
st.set_page_config(page_title="Career & Skill Advisor", page_icon="🎯", layout="wide")

st.sidebar.title("🎯 Career & Skill Advisor")
domain = st.sidebar.selectbox("👉 Choose your domain of interest:", list(career_data.keys()))
hours = st.sidebar.slider("⏰ Study hours per day", 1, 6, 2)

st.title("🚀 Personalized Career Roadmap & Planner")

if domain:
    st.header(f"📌 Roadmap for {domain}")

    col1, col2, col3 = st.columns(3)

    with col1:
        st.subheader("🛠️ Skills to Learn")
        for skill in career_data[domain]["skills"]:
            st.write(f"- {skill}")

    with col2:
        st.subheader("📜 Certifications")
        for cert in career_data[domain]["certifications"]:
            st.write(f"- {cert}")

    with col3:
        st.subheader("🎓 Workshops")
        for ws in career_data[domain]["workshops"]:
            st.write(f"- {ws}")

    st.markdown("---")

    st.subheader("📅 Weekly Study Timetable")
    timetable = generate_timetable(career_data[domain]["skills"], hours)
    for day, task in timetable.items():
        st.write(f"**{day}:** {task}")
```
### css 
```
<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap');

/* Apply Montserrat font globally */
* {
    font-family: 'Montserrat', sans-serif;
}

/* Title style */
.css-10trblm { 
    font-family: 'Montserrat', sans-serif;
    font-size: 32px !important;
    color: #2E86C1;
    font-weight: 700;
}

/* Sidebar style */
.css-1d391kg {
    font-family: 'Montserrat', sans-serif;
    font-size: 16px;
}
</style>
```
### OUTPUT 
An AI which can be accessed anytime anywhere. More affordable than a Human personalized councellor .
