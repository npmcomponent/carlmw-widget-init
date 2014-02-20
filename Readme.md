*This repository is a mirror of the [component](http://component.io) module [carlmw/widget-init](http://github.com/carlmw/widget-init). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/carlmw-widget-init`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*

# widget-init

  initialises widgets bound to DOM elements through a data-attribute hook

## Installation

    $ component install carlmw/widget-init

## Example

    <div id="target" data-require="test-widget" data-foo-bar="baz">Target Element</div>
    <script>
    require.register("test-widget", function(module){
      module.exports = function (el, dataset) {
        // el => div#target
        // dataset => {fooBar: "baz", require: "test-widget"}
      };
    });

    require('widget-init')(document);
    </script>


## License

  MIT
