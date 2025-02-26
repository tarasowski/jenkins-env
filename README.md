# Jenkins Pipeline: Print Global Environment Variables

This Jenkins pipeline demonstrates how to use globally defined environment variables in a Jenkins pipeline.

## 📌 Pipeline Overview

The pipeline consists of a single stage that prints a global environment variable (`MY_GLOBAL_VAR`) that has been set in Jenkins **Global Settings**.

## 🛠️ Prerequisites

- Jenkins installed and configured.
- A Jenkins agent available to run the pipeline.
- A global environment variable (`MY_GLOBAL_VAR`) defined in **Manage Jenkins → Configure System → Global properties → Environment variables**.

## 🚀 Pipeline Script

```groovy
pipeline {
    agent any

    stages {
        stage('Print Global Env Vars') {
            steps {
                echo "My global variable: ${env.MY_GLOBAL_VAR}"
            }
        }
    }
}
