FROM python:3.5-stretch 

COPY requirements.txt ./

RUN apt-get update && apt-get install -y \
    graphviz libgraphviz-dev pkg-config

RUN pip install --upgrade pip \
    && pip install -r requirements.txt

RUN pip install pygraphviz \
    --install-option="--include-path=/usr/include/graphviz" \
    --install-option="--library-path=/usr/lib/graphviz/"

# CMD ["start-notebook.sh", "--NotebookApp.token=''"]
CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--allow-root", "--NotebookApp.token=''", "--NotebookApp.password=''"]