# ArduinoStringToNum
ArduinoStringToNum returns ruby number objects  from strings containing  little-endian binary  representation of a Arduino types.


## Installation

Add this line to your application's Gemfile:

```ruby
gem 'ArduinoStringToNum'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install ArduinoStringToNum

## Usage

Can convert char byte longs ints and floats.

Examples:
    #128,000,000 long from Arduino 
    ArduinoStringToNum.new(00000000001000001010000100000111).to_long
    => 128,000,000
 
    #3460 int from Arduino
    ArduinoStringToNum.new(1000010000001101).to_int
    => 3460

  
    #'a' char from Arduino
    ArduinoStringToNum.new(01100001).to_char
    => a
 
    #128 byte from Arduino
    ArduinoStringToNum.new(10000000).to_byte
    => 128
 
    # 4560 unsigned long from Arduino
    ArduinoStringToNum.new(11010000000100010000000000000000).to_ulong
    => 4560
 
    #2.5 float from Arduino
    ArduinoStringToNum.new(00000000000000000010000001000000).to_ieee754
    => 2.5

 



## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).

