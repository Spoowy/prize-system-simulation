# Affiliate Prize System Simulator
Simulate winner's prices on a percentage-based reward system. 

[Demo](https://spoowy.github.io/prize-system-simulation/index.html)

The first winner gets 50% of his commission back, the second 40%, the third 30% etc.
 
![Preview screenshot](https://raw.githubusercontent.com/Spoowy/prize-system-simulation/master/screenshot.png)

## Configuration
Prizes are auto-generated and percentages can be set here:

    var prizes = [50, 40, 30, 20, 10]; // prizes (percentages), in logical order

The generated list item can also be adjusted:

      listItem.innerHTML = "Place prize (" + percentage + '%) <span class="place-val" id="place-' + prize + '"></span>';

The currency is set in the format function (first return-split-element `"$ "`): 

    function format(n) {
      return "$ " + parseFloat(n).toFixed(2).replace(/(\d)(?=(\d{3})+\.)/g, '$1,');
    }
