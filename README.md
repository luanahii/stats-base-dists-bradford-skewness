# Bradford Distribution Skewness: Understanding Asymmetry in Statistics 📊

![Bradford Distribution](https://img.shields.io/badge/Download%20Release-v1.0.0-brightgreen.svg)  
[Download the latest release here](https://github.com/luanahii/stats-base-dists-bradford-skewness/releases)

## Table of Contents

- [Overview](#overview)
- [Installation](#installation)
- [Usage](#usage)
- [Examples](#examples)
- [API Documentation](#api-documentation)
- [Contributing](#contributing)
- [License](#license)

## Overview

The **Bradford distribution** is a continuous probability distribution that is often used in statistical modeling. It is particularly useful in situations where data exhibit skewness. This repository focuses on the **skewness** of the Bradford distribution, providing tools to calculate and analyze its asymmetry.

### Key Features

- Calculate skewness for the Bradford distribution.
- Easy integration with JavaScript and Node.js applications.
- Comprehensive API for statistical analysis.

## Installation

To install this package, you can use npm. Run the following command in your terminal:

```bash
npm install stats-base-dists-bradford-skewness
```

Once installed, you can require it in your JavaScript or Node.js application:

```javascript
const bradfordSkewness = require('stats-base-dists-bradford-skewness');
```

## Usage

### Basic Calculation

To calculate the skewness of the Bradford distribution, use the following function:

```javascript
const skewness = bradfordSkewness(a, b);
```

Where:
- `a`: Shape parameter of the Bradford distribution.
- `b`: Scale parameter of the Bradford distribution.

### Example

Here’s a simple example to demonstrate how to calculate skewness:

```javascript
const bradfordSkewness = require('stats-base-dists-bradford-skewness');

const a = 2; // shape parameter
const b = 3; // scale parameter

const skew = bradfordSkewness(a, b);
console.log(`The skewness of the Bradford distribution is: ${skew}`);
```

## Examples

### Skewness Calculation

```javascript
const bradfordSkewness = require('stats-base-dists-bradford-skewness');

const examples = [
    { a: 1, b: 1 },
    { a: 2, b: 1 },
    { a: 3, b: 1 },
];

examples.forEach(({ a, b }) => {
    const skew = bradfordSkewness(a, b);
    console.log(`For a = ${a} and b = ${b}, skewness = ${skew}`);
});
```

### Visualizing Skewness

To better understand skewness, you can visualize the Bradford distribution using libraries like D3.js or Chart.js. Below is a simple example using Chart.js:

```html
<canvas id="myChart" width="400" height="400"></canvas>
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<script>
const ctx = document.getElementById('myChart').getContext('2d');
const skewnessData = [/* Data points based on your calculations */];

const myChart = new Chart(ctx, {
    type: 'line',
    data: {
        labels: ['Label1', 'Label2', 'Label3'],
        datasets: [{
            label: 'Bradford Distribution Skewness',
            data: skewnessData,
            borderColor: 'rgba(75, 192, 192, 1)',
            borderWidth: 1
        }]
    },
    options: {
        scales: {
            y: {
                beginAtZero: true
            }
        }
    }
});
</script>
```

## API Documentation

### `bradfordSkewness(a, b)`

- **Parameters**:
  - `a` (number): Shape parameter.
  - `b` (number): Scale parameter.
  
- **Returns**: 
  - (number): The skewness of the Bradford distribution.

### Example API Call

```javascript
const skew = bradfordSkewness(2, 3);
console.log(`Skewness: ${skew}`);
```

## Contributing

We welcome contributions to improve this repository. If you want to help, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes.
4. Commit your changes with clear messages.
5. Push to your branch.
6. Open a pull request.

Please ensure your code adheres to the existing style and includes tests where applicable.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

For further information, check the [Releases](https://github.com/luanahii/stats-base-dists-bradford-skewness/releases) section for updates and version history.