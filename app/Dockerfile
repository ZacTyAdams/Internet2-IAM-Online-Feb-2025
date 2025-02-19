FROM --platform=linux/amd64 python:slim-bookworm

# Install required Python packages
RUN pip3 install langchain langchain-ollama

# This is to keep the container up and running
CMD ["sleep", "infinity"]