# DreamBooth Action

This is a template repo for **training and publishing your own custom [DreamBooth](https://replicate.com/blog/dreambooth-api) model** using Replicate and GitHub Actions.

## Preqrequisites

- A paid [Replicate](https://replicate.com/account) account
- A handful of training images

## Training the model

🍿 Like to learn by watching? Check out the [video tutorial on YouTube](https://www.youtube.com/watch?v=jknKfY13LbY)

1. 🐣 Create your own copy of this repository by clicking the green "Use this template" button, then "Create a new repository". Name your new repository whatever you like, and choose whether you want to make it public or private.
1. 🐕 Remove the cute puppy images in the [data](data) directory and replace them with your own images.
1. 💾 Commit your changes to git and push to your main branch on GitHub.
1. 🕵️‍♀️ Copy your Replicate API token from [replicate.com/account](https://replicate.com/account) and [create a repository secret](https://docs.github.com/en/actions/security-guides/encrypted-secrets#creating-encrypted-secrets-for-a-repository) named `REPLICATE_API_TOKEN`.
1. 🎬 Trigger the workflow from your GitHub repo page: "Actions" > "Train a model" > "Run workflow".
1. Go to the [replicate.com](https://replicate.com) homepage. At the top of your list of predictions, you'll see a replicate/dreambooth prediction in progress. This the request to train your model. Click that prediction to see the progress of the training process.
1. ☕️ Grab a coffee or a snack and watch the logs roll by! The training process takes a few minutes to run.

## Running the model

Depending on the number of training steps you specified when running the workflow, the training process can take 10-40 minutes to run. 

When the training process has completed successfully, it pushes the model to Replicate. You can run it like any other Replicate model, using the website or the API.

To run on the website, go to [your dashboard](https://replicate.com) then click on "Models".

Your new model will be private by default, and only visible to you. If you want anyone to be able to see and run your model, you can make it public in the Settings tab on your model page.

To run the model on the web, enter a prompt using the identifier you specified during training, e.g. `a pencil sketch of zxz`.

To run the model from your own code, click the API tab on your model page for instructions on running with Python, cURL, etc.

To learn more about running models on Replicate, take a look at the [Python getting started guide](https://replicate.com/docs/get-started/python) or the [HTTP API reference](https://replicate.com/docs/reference/http).

If you have questions, open an issue on this repo or find us in [Discord](https://discord.gg/replicate).