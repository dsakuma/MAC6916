FROM python:3.5-stretch 

COPY requirements.txt ./
RUN pip install --upgrade pip \
    && pip install -r requirements.txt

# CMD ["start-notebook.sh", "--NotebookApp.token=''"]
CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--allow-root"]