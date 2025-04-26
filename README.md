# NitoFacts - JSON Web Service

Provides NitoFacts in JSON format. Supports multiple languages and live data.

IMPORTANT: NitoFacts are currently under development, and are subject to change. They are currently only available in English as they still being written. Please check back in a week or two.

## About NitoFacts

NitoFacts are bitesize facts about the [Nito](https://nito.org) blockchain, designed to be embedded in apps and websites, and shared across social media.

They are provided in JSON format, so it is easy for developers to use them in their projects and help educate their users about Nito. This format also ensures they can be easilly updated and expanded in the future.

## Usage

- NitoFacts are available in multiple languages and in multiple formats - social (default), html and markdown (see below).
- For Wordpress users, there is a plugin available [here](https://github.com/Nito-Tools/NitoFacts-Wordpress-Plugin) that makes it easy to add the NitoFacts to your website.
- Query the JSON URL for the desired language and format, not more than once every 60 minutes, and cache the results locally.
- It is suggested to display a random NitoFact once per minute, or whenever the page reloads.
- **IMPORTANT: Several of the NitoFacts include dynamic data (see below) and must be updated periodically so that they remain accurate - querying the server once every hour per language should be sufficient. Please do not exceed this by making too many frequent requests to avoid stressing the server.**

For more help, visit: https://nitofacts.nito.tools/?help

| Language               | JSON URL                                                           | 
|------------------------|--------------------------------------------------------------------|
| English                | https://nitofacts.nito.tools/?lang=en&format=social             |
| Chinese (Simplified)   | https://nitofacts.nito.tools/?lang=zh&format=social             |
| Russian                | https://nitofacts.nito.tools/?lang=ru&format=social             |     
| Spanish                | https://nitofacts.nito.tools/?lang=es&format=social             |
| Korean                 | https://nitofacts.nito.tools/?lang=ko&format=social             |
| Japanese               | https://nitofacts.nito.tools/?lang=ja&format=social             |
| German                 | https://nitofacts.nito.tools/?lang=de&format=social             |
| French                 | https://nitofacts.nito.tools/?lang=fr&format=social             |
| Portuguese             | https://nitofacts.nito.tools/?lang=pt&format=social             |
| Hindi                  | https://nitofacts.nito.tools/?lang=hi&format=social             |
| Dutch                  | https://nitofacts.nito.tools/?lang=nl&format=social             |
| Italian                | https://nitofacts.nito.tools/?lang=it&format=social             |

### Requesting Diferent Formats

- ```format=social``` displays any links with the URL inline. This makes them ideal for sharing on social media.<br>e.g. ```Click here for more: https://example.com``` 
- ```format=html``` displays any links as HTML. This makes them ideal for embedding in web pages.<br>e.g. ```Click <a href="https://example.com">here</a> for more.```
- ```format=markdown``` displays any links as markdown syntax.<br>e.g. ```Click [here](https://example.com) for more.```

## Contributions

Contributions to this project from the community are actively encouraged. If you notice NitoFacts that are out of date or erroneous, please fork the repo and make a PR. You can also create an Issue [here](https://github.com/Nito-Tools/NitoFacts-JSON/issues). 

### Adding new NitoFacts

Everybody is encouraged to help contribute new NitoFacts. If you have a Nito project that you wish to make the community aware of, please add a new NitoFact. Be careful to use neutral wording - no marketing or advertisng is permitted, though a single Nitoact to tell the community about your project and what it does is permitted.

Important considerations:
- New NitoFacts must be added in English first. This will then be used as the basis for the translation into other languages.
- URLs should be included both within the content text, and in the seperate URL field. This allows for easier processing. Please include only one URL per NitoFact.
- NitoFacts about price will not be accepted - they are for educating the community about Nito only.

### Using Live Data in the NitoFacts

If you wish to insert live data into a NitoFact, please edit the nitofacts.json file and insert any of the following variables:

| Variable        			     | Example Content   | Note                                                |
|--------------------------------|-------------------|-----------------------------------------------------|
| ```$block_height```            | 1,238,764         | Displays the current number of Nito blocks, with comma seperator.  |
| ```$blocks_tot_mil```          | 1.2               | Displays the current number of Nito blocks rounded to the nearest 0.1 million. |
| ```$circ_supply```             | 203,986,880       | The current circulating supply of NITO. | 
| ```$circ_supply_percent```     | 18.25%            | The current circulating supply of NITO as a percentage of the total. | 
| ```$block_reward_current```    | 512               | The current Nito block reward. | 
| ```$block_reward_next```       | 256               | The next Nito block reward (after the next halving). | 
| ```$next_halving_date```       | 3 September 2025  | The date of the next halving  | 
| ```$next_halving_time```       | 14:32 UTC         | The time of the next halving   | 
| ```$next_halving_days```       | 225               | Days remaining till the next halving   | 
| ```$milestone_next_date```     | 29 July 2026      | The date of the next halving  | 
| ```$milestone_next_time```     | 16:29 UTC         | The time of the next halving   | 
| ```$milestone_next_days```     | 502               | Days remaining till the next halving   | 


These variable will be replaced by live data every minute.

## Disclaimer

These NitoFacts are provided by the Nito community for the Nito community. It is up to the community to ensure they are current and accurate. Please make a PR with any corrections or create an Issue.

Users should always do their own due diligence before using any of the services or products mentioned in these NitoFacts. They are provided for information purposes only - mentions are not endorcements.



