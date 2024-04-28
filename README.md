# wynncraft-GPS

wynncraft GPS for map coordinate

## install 
wyyncraft-GPS

follow the instruct before running the script 

1. 

move the place.xml AND map.xml to the folder to C:\USERS\(USERNAME)

2.

run

```
start $profile in powershell
```

copy the completer function to your profile.ps1

```
# <auto argument completers for GPS>
function MyArgumentCompleter{
    param ( $commandName,
            $parameterName,
            $wordToComplete,
            $commandAst,
            $fakeBoundParameters )

    $possibleValues = @{
        find = @("'potion merchant'",'blackSmith',"'scroll merchant'",'farm','fishing',"'tool merchant'",'cave','mine','identifier','bank','chest','powder master','housing','gold','iron','redstone')
        remove = @()
        add = @("'potion merchant'",'blackSmith',"'scroll merchant'",'farm','fishing',"'tool merchant'",'cave','mine','identifier','bank','chest','powder master','housing','gold','iron','redstone')
    }

    if ($fakeBoundParameters.ContainsKey('action')) {
        $possibleValues[$fakeBoundParameters.action] | Where-Object {
            $_ -like "$wordToComplete*"
        }
    } else {
        $possibleValues.Values | ForEach-Object {$_}
    }
}

````
			

## arguments 

1.gps.ps1 find [type]



![image](https://github.com/CN-CODEGOD/wynncraft-GPS/assets/166476136/8e2b5064-c5fe-4d30-918e-82e227af6162)

usage: 

find the  near place around you by passing x,y,z 


2.gps add [type] 

![image](https://github.com/CN-CODEGOD/wynncraft-GPS/assets/166476136/0bacaecb-257d-4d89-bc5e-af9714b77a34)

usage: 

add the new place for the script,will add the type will be the [type] of new adding place

3. gps remove

   ![image](https://github.com/CN-CODEGOD/wynncraft-GPS/assets/166476136/d6105105-41ef-46e0-a36b-826db714dd5b)

   usage :

   remove the places adding to your script by passing the id 


4. gps calc


![image](https://github.com/CN-CODEGOD/wynncraft-GPS/assets/166476136/1bbe5c9a-812f-415a-9ff5-dd56d87d541a)

   
usage :

calc the nearest town between town and your destination by passing xyz


