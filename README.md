snappy Ruby
===========

This is a simple demonstration on how to use the snappy gem written by miyucy at [https://github.com/miyucy/snappy](https://github.com/miyucy/snappy). It has two dependencies to the standard Ruby libraries [OpenStruct](http://www.ruby-doc.org/stdlib-2.0/libdoc/ostruct/rdoc/OpenStruct.html) and [OptionParser](http://ruby-doc.org/stdlib-2.1.0/libdoc/optparse/rdoc/OptionParser.html).

Usage
-----

    Usage: snappy [options] input_stream [output_file]
        -d, --deflate                    Deflate a given input stream
        -i, --inflate                    Inflate a given input stream
        -s, --stream STREAM              Input stream
        -o, --output OUTPUT              Output file
        -h, --help                       Show this message

Examples
--------

### Deflate a file

    ./snappy -d -s example_file

    Summary:
      original file size: 0.0217 MiB
      compressed file size: 0.0117 MiB

=> example_file-1394896776.sn

### Deflate a string

    ./snappy -d -s "I am a string and I am just here for demonstration ya know"

    Summary:
      original file size: 0.0566 KiB
      compressed file size: 0.0566 KiB

=> I am a string and I am just here for demonstration ya know-1394896955.sn

### Inflate a file

    ./snappy -i -s example_file-1394896776.sn

    Summary:
      original file size: 0.0117 MiB
      compressed file size: 0.0217 MiB

=> example_file-1394896776

Contributing
------------

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
