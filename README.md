# TLADS - Think Like a Data Scientist

## Overview

**TLADS** (Think Like a Data Scientist) is an interactive workshop designed to give participants hands-on experience with data science methodologies and approaches. This project demonstrates the fundamental differences between a software engineer's "Builder's Mindset" and a data scientist's "Experimenter's Mindset" through practical exercises using real-world datasets.

## Author
- **Stephen Webb** - Workshop Creator and Data Science Instructor

## Team
- **Kartheek Palepu**
- **Arunava Ghosh**
- **Anshuman Bhadauria**
- **Anish Ganguli**
- **Rupali KaPatel**
- **Vikesh Singh Baghel**

## Workshop Objectives

By the end of this workshop, participants will:
- Understand how data scientists approach open-ended problems
- Gain first-hand experience tackling exploratory data analysis
- Learn the difference between engineering and scientific problem-solving approaches
- Apply data visualization techniques using modern Python libraries
- Navigate common pitfalls in data science projects

## Project Structure

```
TLADS/
├── .devcontainer/
│   ├── devcontainer.json         # Development container configuration
│   └── Dockerfile                # Container build instructions
├── tlads_nb.ipynb                # Primary workshop notebook (framework)
├── data
│   └── spaceship-titanic
|   │   └── train.csv             # Data used for the workshop
├── docker-compose.yml            # Docker composition for easy setup
├── requirements.txt              # Python dependencies
└── README.md                     # This file
```

## Datasets Included

- [Data](https://www.kaggle.com/competitions/spaceship-titanic/data) has passengers who travelled in a Spaceship Titanic and had a collision with the spacetime anomaly. Some passengers are transported to the desination and some didn't. You're given a set of personal records recovered from the ship's damaged computer system.

### File and Data Field Descriptions
- `train.csv` - Personal records for about two-thirds (~8700) of the passengers, to be used as training data.

**Independent variables**
- `PassengerId` - A unique Id for each passenger. Each Id takes the form gggg_pp where gggg indicates a group the passenger is travelling with and pp is their number within the group. - People in a group are often family members, but not always.
- `HomePlanet` - The planet the passenger departed from, typically their planet of permanent residence.
- `CryoSleep` - Indicates whether the passenger elected to be put into suspended animation for the duration of the voyage. Passengers in cryosleep are confined to their cabins.
- `Cabin` - The cabin number where the passenger is staying. Takes the form deck/num/side, where side can be either P for Port or S for Starboard.
- `Destination` - The planet the passenger will be debarking to.
- `Age` - The age of the passenger.
- `VIP` - Whether the passenger has paid for special VIP service during the voyage.
- `RoomService`, FoodCourt, ShoppingMall, Spa, VRDeck - Amount the passenger has billed at each of the Spaceship Titanic's many luxury amenities.
- `Name` - The first and last names of the passenger.

**Target variable**
- `Transported` - Whether the passenger was transported to another dimension. This is the target, the column you are trying to predict.

#### Optional
- `test.csv` - Personal records for the remaining one-third (~4300) of the passengers, to be used as test data. Your task is to predict the value of Transported for the passengers in this set.

## Getting Started

### Prerequisites

- Docker and VS Code with Dev Containers extension, OR
- Python 3.11+ with pip

### Option 1: Using Dev Container (Recommended)

1. **Clone the repository** and open in VS Code
2. **Reopen in Container** when prompted (or use Command Palette: "Dev Containers: Reopen in Container")
3. **Wait for setup** - dependencies will be installed automatically from `requirements.txt`
4. **Open** `tlads_nb.ipynb` and start the workshop!

### Option 2: Using Docker Compose

```bash
# Clone and navigate to the project
git clone <repository-url>
cd TLADS

# Start the development environment
docker-compose up

# Access Jupyter at http://localhost:8888
```

### Option 3: Local Python Environment

1. **Create a virtual environment**:
   ```bash
   python -m venv tlads-env
   source tlads-env/bin/activate  # On Windows: tlads-env\\Scripts\\activate
   ```

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Launch Jupyter**:
   ```bash
   jupyter notebook tlads_nb.ipynb
   ```
## Key Python Libraries Used

- **pandas** (~2.2.3): Data manipulation and analysis
- **matplotlib** (~3.10.0): Static plotting and visualization
- **plotly** (~5.17.0): Interactive visualizations and dashboards
- **dash** (~2.17.0): Web applications for Python analytics
- **scikit-learn** (~1.5.0): Machine learning library
- **scipy** (~1.14.1): Scientific computing
- **seaborn** (~0.13.0): Statistical data visualization
- **jupyter** (~1.0.0): Interactive notebook environment

## License

This educational material is provided for workshop and learning purposes. Please respect the data sources and attribution requirements.

---

*"In science, if you know what you are doing, you should not be doing it. In engineering, if you do not know what you are doing, you should not be doing it."* - Richard Hamming

Happy Data Science! 🔬📊🐍