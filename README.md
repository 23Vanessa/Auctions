# trustfi-js

trustfi-js is package to integrate TrustFi Ethereum Integrations

## Installation

Use the package manager [npm] to install npm.

```bash
npm i trustfi-js
```

## Usage

```javascript
import moment from 'moment';
import Application from 'trustfi-js/models';

/* Test Version */
let app = new Application({test : true});

/* Create Contract */
let swapContract = app.getFixedSwapContract({tokenAddress : '0x3237fff7f25a354f68b2054a019c5a00135a8955', decimals : 18});

/* Deploy */
await swapContract.deploy({
    tradeValue : 0.001, 
    tokensForSale : 100, 
    startDate : moment().add(6, 'hours'),
    endDate : moment().add(16, 'hours')
});
```
## License

[MIT](https://choosealicense.com/licenses/mit/)
