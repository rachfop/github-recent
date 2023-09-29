# github-recent

Connects to the Temporal Cloud
Runs a Worker on Render

## Render | Run Workers in the Cloud

Run Workers in the Cloud.

The following guide configures and deploys your Temporal Workers on Render (render.com).

For a complete set of documentation see https://render.com/docs

For documentation on background workers, see https://render.com/docs/background-workers

### Configure background workers

1. Select `New workers`.

[Background Workers](https://render.com/docs/background-workers) are suitable for long running processes like consumers for queues and streaming.

1. Choose one of the following and add your repository:
    1. **Build and deploy from a Git repository**
    2. **Deploy an existing image from a registry**
2. On the `Create Background Worker` page, enter the following informaiton:
    1. Name: the name of your background worker.
    2. Region: the region where you background worker runs.
    3. Branch: the repository branched used for you background worker. (`main`)
    4. Runtime: The runtime for your background worker. (`Python 3`)
    5. Build Command: the command that runs in the root directory. (`pip install -r requirements.txt`)
    6. Start Command: the command that runs your worker. (`python3 run_worker.py`)
3. Select your instance type.

Continue to add your secrets.

### Set up secrets

1. Select `Advanced ^` and choose either:
    1. `Add Environment Variable`
        1. Enter a key and a value.
    2. `Add Secret File`
        1. give your filename a name.
        2. enter the file contents.
        3. Choose `Save`.

Continue to deploy your Worker.

### Deploy worker

1. Choose `Create background Worker` when you’re ready.

Review your logs.

## Review deployment

1. From the logging dashboard, watch your worker deploy.
2. You should see something similar to the following:

