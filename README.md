# Ocean Collective Cred Scoring

Tooling to compute Cred scores for the Ocean Collective using the [Sourcecred](https://sourcecred.io/) social algorithm.

![generate-cred](https://github.com/Ocean-Collective/cred/workflows/generate-cred/badge.svg)

## Requirements

* Node (10.x.x - 12.x.x)
* Yarn
* Serve (npm -i -g serve) (To deploy the Frontend graph locally)

## Local Setup Instructions

```bash
git clone https://github.com/sourcecred/sourcecred.git
cd sourcecred
yarn install
```

## Configuration

*See [Spec](projects/collective.json)*

* Sources
  - Ocean Protocol Official [Discourse](https://port.oceanprotocol.com) forum (AKA Port)
  - [Ocean Collective Github Org](https://github.com/Ocean-Collective)
* Weights [Spec](weights.json) (WIP **NOT Active** using defaults)
  - Edges
    - 
  - Nodes
    - 

## Computing Cred

Cred Scores can be updated locally by running the following commands:

```Bash
export SOURCECRED_GITHUB_TOKEN=YOUR_GITHUB_TOKEN # You can generate a personal API Token here -> https://github.com/settings/tokens
export sc=PATH_TO_YOUR_SOURCECRED_LOCAL_REPO
./update.sh
serve ./docs # Frontend will be available at http://localhost:5000
```

## Generate-Cred Github Action

The Github [action](.github/workflows/generate-cred.yml) is in charge of both re-computing the Community Cred scores and updating the Public [UI Graph](https://ocean-collective.github.io/cred/timeline/@ocean-collective/) every week (Sun at 23:59)

## License

* Apache License, Version 2.0, ([LICENSE](LICENSE) or <https://www.apache.org/licenses/LICENSE-2.0>)




