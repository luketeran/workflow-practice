name: Simple Continuous Integration

on: 
  push:
    branches: [main]

jobs:
  build:
    name: Build and Test for Integration
    runs-on: Ubuntu-latest
    steps:
    - uses: actions/checkout@v4
    - uses: actions/setup-python@v4
      with: 
        python-version: '3.10'

    - name: install plugin
      run: |
        pip install pytest pytest-cov
    - name: checkout my codes
      uses: action/checkout@v4
      with:
        repository: luketeran/workflow-practice

    - name: 
    
