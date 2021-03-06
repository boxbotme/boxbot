# BoxBot
This is the central repository housing all components for BoxBot into one functional application.

## Modules
* BoxBot Core API by @justinpotts
* BoxBot.me Website by @OhNoYouSquidnt
* Boxcutter Texting API by @jeffw16 (integrated into BoxBot)

## Requirements for each module
* BoxBot Core API
 * Flask
 * SQLAlchemy
 * Werkzeug
* BoxBot.me Website
 * Uses Bootstrap 3 (included)
* Boxcutter Texting API
 * Twilio Helper Library (Python)

## Install and Run

### Setup

#### VirtualEnv

Though not required, we recommend you use VirtualEnv. This will allow you to better manage and separate packages from other projects, enabling you to install different versions across your environments.

    pip install virtualenv
    virtualenv venv

To activate your Virtual Environment, run the command:

    source venv/bin/activate

#### Requirements

To install the dependencies, run `pip install -r requirements.txt`.

#### Database

To interact with users (signing in, joining, etc..) you'll need to set up a database on your machine.

    python

    >>> from app import db
    >>>
    >>> db.create_all()

After making changes to the database structure, or if you want to start with a clean slate, run `rm /tmp/boxbot.db`.

WARNING: Database will be deleted upon computer shutdown or sign off. Do not store valuable data without a backup in the temporary database.

### Run

    python app.py

Output:

     * Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
     * Restarting with stat
