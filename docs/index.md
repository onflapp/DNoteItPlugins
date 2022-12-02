# Create new plugin

DNoteIt plugin is executable shell script that starts with 'filter_' and ends with '.txt' extension. For example 'filter_test.txt'
You can create the plugin in any text editor, just make sure you make it **executable**.

Downloading and modifying one of the [sample plugins](https://github.com/onflapp/DNoteItPlugins) is good way to start start.

# Sample Plugin

DNoteIt plugin is a shell scripts that read data from input (optional) and writes to output. The output can by any valid MD markup, including HTML.
The shell script will be executed with following arguments:

- $1 - temporary directory containing the main .md file
- $2 - real path pointing the dnote document

The plugin is invoked by looking up a name of *fenced code block* and passing its content (if relevant) as stdin.
The name itself should not include 'filter_' prefix, nor extension '.txt'.

For example

<pre>
```mydate
  date
```
</pre>

would invoke script *filter_mydate.txt* and inserting current date in place of the fenced code block.

# Where do I find the Scripts folder?

The scripts folder is under your home folder **Library/Application Scripts/com.onflapp.DNoteIt-Mac**
You can use Finder to go there directly:

1. select menu "Go", then "Go to Folder"
2. type in '~/Library/Application Scripts/com.onflapp.DNoteIt-Mac'
3. If this folder does not exist already, create it.
