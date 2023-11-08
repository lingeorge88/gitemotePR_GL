# GitEmote GitHub Action

GitEmote is a GitHub Action that adds an emote reaction to new pull requests based on their titles. It's a fun way to express your emotions and engagement with incoming changes!  This is a modified action based off of the original [PR Emote Generator](https://github.com/rcmtcristian/gitemote) action created by [@rcmtcristian](https://github.com/rcmtcristian)

## Usage

To use GitEmote in your repository, follow these steps:

1. Create a `.github/workflows/gitemote.yml` file in your repository.

2. Add the following code to the `gitemote.yml` file:

```yaml
name: GitEmote

on:
  pull_request:
    types:
      - opened

jobs:
  gitemote:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout Code
        uses: actions/checkout@v2

      - name: Run GitEmote
        uses: lingeorge88/gitemotePR_GL@main
        with:
         GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

Now, whenever someone creates a new pull request in your repository with a title containing the specified keywords, GitEmote will react with the chosen emote.

Currently supported keywords are :`fix`, `feat`, `style`,`refactor`, `docs`, `test`
### Preview

![Screenshot 2023-11-07 at 8 13 31 PM](https://github.com/ProgramEquity/amplify/assets/115956879/45fc82c9-60d1-462e-822f-ce9dff37b289)
![Screenshot 2023-11-07 at 8 16 15 PM](https://github.com/ProgramEquity/amplify/assets/115956879/079e42f8-1a27-4038-a641-d85abc4f1d73)
![Screenshot 2023-11-07 at 8 22 16 PM](https://github.com/ProgramEquity/amplify/assets/115956879/d1d8447b-ef4d-4ad8-b0e3-41fc08420475)
![Screenshot 2023-11-07 at 8 24 26 PM](https://github.com/ProgramEquity/amplify/assets/115956879/ffee58aa-9073-4406-a922-6305cafa01e5)
![Screenshot 2023-11-07 at 8 25 24 PM](https://github.com/ProgramEquity/amplify/assets/115956879/1dcbbddb-4381-4ba3-bc91-bf9c36d35fd2)

