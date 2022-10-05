# Dashboards

The [`topics`](./topics.md) and [`docker`](./venues.md) dashboards allow for detailled views on either property.

Here is some example code.

=== ".csi/workflows.yaml"

    ```yaml
    workflows:
      - name: hello-fastapi
        provider: bash
        ports: 1
        commands:
          - pip install fastapi uvicorn
          - uvicorn hello_fastapi:app --port $PORT_0 --host 0.0.0.0
    ```

=== "hello_csi.py"

    ```python
       from fastapi import FastAPI
       
       app = FastAPI()
       
       
       @app.get("/")
       async def root():
           return {"message": "Hello World"}
    ```

!!! info "NOTE:"
    Here is something important to note.
    Just like in the previous example, this is a note.
    