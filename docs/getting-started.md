# Getting Started

This guide walks new learners through the steps to set up their development environment, access the curriculum, and start the first week.

## Prerequisites

- A recent Linux distribution (Fedora, Ubuntu, etc.)
- Git
- Python 3.11+ and `pip`
- Node.js 20+ and `npm`

## Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/Geddywendot/Software-Engineering.git
   cd Software-Engineering
   ```
2. **Create a virtual environment**
   ```bash
   python -m venv .venv
   source .venv/bin/activate
   ```
3. **Install documentation dependencies**
   ```bash
   pip install -r requirements.txt
   ```
4. **Build the site locally**
   ```bash
   mkdocs serve
   ```
   Open `http://127.0.0.1:8000` in a browser.
5. **Read the first week**
   Navigate to **Week 1 – Git Mechanics & The Unix Philosophy** under the *Foundations* section.

Happy learning!
