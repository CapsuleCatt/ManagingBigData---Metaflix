# Team 13 - Metaflix
### Team members: 
**Aimee Chen, Zhizhi Wang, Samy Dushimimana Shyaka, Jason Evans**
## Target Company: Netflix 
 
The application demo is built with **Streamlit**. The application includes features such as user authentication, homepage, a friend system, and watch-together sessions. It uses **MongoDB Atlas** for storing movie data, friend data, and watch history, and supports additional integration with **AWS RDS** for relational data like user data, etc., and live comments data is stored in **HBase** due to the huge data amount.

## Features
- **User Authentication**: Secure login and logout functionality.
- **Homepage**: Featured movie recommendations, trending content, and movie details.
- **Friend System**: Add and manage friends.
- **Watch Together**: Watch shows with friends and chat.
- **Account Management**: Update account settings and view user details.

## Easy Access to Demo
- **[Demo App (Click to access)](https://metaflix.streamlit.app/)**

## Tech Stack
- **Frontend**: [Streamlit](https://streamlit.io/)
- **Backend**: 
  - MongoDB for movie data, friend data, and watch history data
  - AWS RDS for relational data
  - HBase for live comments data (Due to the EMR cluster setup, the HBase part is not included in the demo app)

- **Python Libraries**:
  - See details in requirements.txt
- **Deployment**: Streamlit Cloud

## Installation
### Prerequisites
1. Python 3.7+
2. MongoDB database (Atlas or local setup)
3. AWS RDS for additional data storage
4. Install required Python libraries:
   ```bash
   pip install -r requirements.txt
   ```

### Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/netflix-app.git
   cd netflix-app
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Set up your MongoDB or RDS credentials in `secrets.toml`:
   ```toml
   [mongodb]
   connection_string = "your_mongodb_connection_string"
   database_name = "netflix_db"

   [rds]
   db_host = "your-rds-endpoint.amazonaws.com"
   db_user = "your_database_name"
   db_password = "your_username"
   db_name = "your_password"
   ```

4. Run the app:
   ```bash
   streamlit run __init__.py
   ```

## File Structure
```
netflix-app/
│
├── __init__.py           # Main entry point of the app
├── .streamlit/           # Streamlit configuration (Ignored in Git)
│   └── secrets.toml      # Credentials for MongoDB and RDS 
├── login_config.py       # Login configuration
├── home.py               # Logic for the Homepage
├── friends.py            # Logic for the Friends system
├── watch_together.py     # Logic for the Watch Together feature
├── accounts.py            # Logic for the Account Management
├── requirements.txt      # Dependencies
├── README.md             # Project documentation
└── moviecover.jpg        # Sample movie cover image
```

## Deployment
1. Push the code to your Git repository.
2. Set up your app on **Streamlit Cloud**.
3. Add secrets in Streamlit's **Secrets Manager** under the "Advanced settings" section.