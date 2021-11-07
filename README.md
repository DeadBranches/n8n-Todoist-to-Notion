# n8n-Todoist-to-Notion

A workflow for the automation tool [n8n](https://n8n.io/). Facilitates using Todoist's UI to input data into Notion database pages and/or page blocks.

# The Problem it Solves

On mobile there's an appreciable delay for opening/loading a desired location in Notion before getting to the point of data input. In contrast, Todoist's android widget opens immediately upon click. This workflow allows Todoist to be our input for Notion saving all that time spent waiting. It makes recording fleeting idea and notes into Notion more feasible. 

# How it Works

1. The workflow recieves webhook notifications from Todoist when a new task is added or updated.
2. Based on which Todoist project the task was added to, the task's content and description is then added as a database page or page block by using Notion's integration function.
3. The initial task is deleted from Todoist. 

![Image of the workflow](https://i.imgur.com/J47tLBL.jpeg)

# What's Required.

- A local or hosted n8n installation

# Configuration

## Credentials

The user is required to setup and configure n8n for both Todoist and Notion credential authentication. Instructions for Todoist credentials can be found [here](https://docs.n8n.io/credentials/todoist/). Notion's credential documentation is found [here](https://docs.n8n.io/credentials/notion/#prerequisites).

## Defining Todoist Project ids

Each **If** block defines the Todoist project id that will trigger the Notion actions that follow the if block.

## Defining Notion database/page/block ids

This is done individually for each Notion block.
