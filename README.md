# Demo AWS Lambda container image

## Install dependencies

1. Install `virtualenv`

    You can skip this step if you have already installed `virtualenv` on your system.

    ```
    pip install virtualenv
    ```

2. Create a `venv` directory (require Python 3.8) and activate it:

    ```
    virtualenv venv
    .\venv\Scripts\activate
    ```

3. Install dependencies

    ```
    pip install -r requirements.txt
    ```

## Build & Run the container

1. Build the container image:

    ```
    docker build -t aws-lambda-demo:latest .
    ```

    You can skip this step if you have already built the container image.

2. Run the container:

    ```
    docker run -p 9000:8080 aws-lambda-demo:latest
    ```


## Local testing

```
curl -XPOST "http://localhost:9000/2015-03-31/functions/function/invocations" -d '{}'
```