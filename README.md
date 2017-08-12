cache
=====

###Simple shell caching

The aim of this function is to make it easy to take a process which takes a long time to process and store it for future use. It is easy to utilize and greatly improves the performance of some applications.

###Utilizing Cache

Once you have downloaded the code to an accessible location you need to source it into your current shell:

```
. ${HOME}/lib/cache
```

Now with the function sourced you can begin to cache data

```
Output=$(Cache ${Key} || OutputCommand ${Key} | Cache ${Key})
```

The above command does 2 things. First it asks Cache if data is available for the requested Key, if Cache returns non 0 then run a command that generates output and pipe it into Cache along with the Key to be stored for later use.




