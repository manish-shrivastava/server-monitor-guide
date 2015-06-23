# Server-monitor-guide
This guide explains How to Monitor Apache Web Server Load and Page Statistics.

You might have often wanted to be able to see real-time hits as they arrive. Well, **Google Analytics** is a wonderful package for looking at trends over time, but there’s a delay of a few hours there, and you really can’t see data like requests per second or total bytes.

There is some server based tools guide for apache server monitor guide.

## Apachetop 
 
[apachetop](https://github.com/JeremyJones/Apachetop) is a console-based tool for monitoring the threads, monitor traffic real-time and overall performance of a set of Apache web servers.

### Installation

#### Installing on Ubuntu
`apt-get install apachetop`

#### Installing from Source on CentOS
```
wget http://www.webta.org/apachetop/apachetop-0.12.6.tar.gz

yum install readline-devel

yum install ncurses-devel

tar xvzf apachetop-0.12.6.tar.gz

cd apachetop-0.12.6

./configure

make

```


### How to use

#### Assign Access log to apachetop

You can launch it by simply running `apachetop` from the console/terminal. You can pass in the -f parameter to specify the location of the logfile. 

`apachetop -f /var/log/apache2/access.log`

#### To Monitoring Time frame

It Will display stats on the last x number of hits

`apachetop -H hits`

 It will display stats on the last x number of seconds
 
`apachetop -T secs`


#### Filters

To access the filters, use the key: `f`
It will prompt to ask you options (a, b, c ) for the filter.
Hit the `a key` to add a filter and the line should switch. Now you can choose to filter by `URL`, `referrer`, or `host`.


### Help

At any point you can hit the `?` or the `h key` to take you to the help screen, which will give you a quick view of all the options.


Thanks,
Manish
