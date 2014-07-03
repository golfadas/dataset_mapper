# Dataset Mapper

![IST Logo](http://tecnico.ulisboa.pt/img/tecnico.png)

Simple modules that map twitter dataset stored in CSV to easy to use arrays and gives you a small resume.

## How to use

Load modules and specify dataset path:

~~~ruby
require_relative "../lib/dataset_mapper.rb"
include DatasetMapper

@dataset_path = '/src/thesis/inesc_data_set_sample/decompressed' 
@base_file = 'tweets01_aaaa'
@default_data = :with_stem
~~~

Get the array if tweets in the dataset:
~~~ruby
tweets       # => array full of tweets
tweets.first # => 'paintbrush work ipad sensubrushman' 
~~~

Get the dataset stats:
~~~ruby
puts inspect_dataset_stats() # =>
# total number of tweets,                 87558
# number of tweets in selected words,     425
# number of words in the dataset,         50880
# number of words used in sample,         18
# number of word ocurrences in sample,    463
# percentil used,         0.94
# words used,             ["recogn", "bracket", "basket", "mar", "length", "initi", "dye", "eras", "tradit", "liverpol", "delici", "advantag", "robot", "potus", "belief", "volum", "hok", "thirstythursday"]
~~~

## Dataset Format
This code was used with other gems not yet published ( sorry about that :p ), used to manipulate the initial dataset in json. It expects a dataset with following structure.

![Dataset Files](https://photos-3.dropbox.com/t/0/AAAqwKhNWq4aAAArxp8ZfxgeUvFx6NJojuXBsZvcvJaNfg/12/3217572/png/1024x768/3/1404396000/0/2/Screen%20Shot%202014-07-03%20at%2013.08.24.png/SGXIz-csRI3gIRcBk-L6o3vpuVjRivfFxd3xhZfLvzU)


## License

This code is released under the [MIT License](http://www.opensource.org/licenses/MIT).