# Cryptocurrency Monitor
Python scripts to monitor cryptocurrencies.
- `yfinance` - Get currency information using yahoo finance [API](https://pypi.org/project/yfinance/)
- `requests` - Get all cryptocurrencies from [yahoo finance](https://finance.yahoo.com/)
- `BeautifulSoup` - Extract tag values from html response
- `SMTP` - Send SMS notification using Simple Mail Transfer Protocol

### Requirements
`pip install --no-cache --upgrade -r requirements.txt`

### Docker
`docker build -t crypto .`<br>
`docker run crypto`

<h6>
Note: DO NOT use <code>alpine</code> for docker as the build dependencies from 
<a href="https://pypi.org/simple/pandas/">simple/pandas</a> fail due to missing pre-req.<br><br>
Alternative is to use <code>slim</code> or install the modules directly from <code>alpine</code> 
<a href="https://pkgs.alpinelinux.org/packages?name=*pandas">repository</a>
</h6>

#### Coding Standards
Docstring format: [`Google`](https://google.github.io/styleguide/pyguide.html#38-comments-and-docstrings) <br>
Styling conventions: [`PEP 8`](https://www.python.org/dev/peps/pep-0008/) <br>
Clean code with pre-commit hooks: [`flake8`](https://flake8.pycqa.org/en/latest/) and 
[`isort`](https://pycqa.github.io/isort/)

#### Linting
`PreCommit` will ensure linting, and the doc creation are run on every commit.

**Requirement**
<br>
`pip install --no-cache --upgrade sphinx pre-commit recommonmark`

**Usage**
<br>
`pre-commit run --all-files`

