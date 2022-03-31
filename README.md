# ESX Legacy
![Lua](https://img.shields.io/badge/lua-%232C2D72.svg?style=for-the-badge&logo=lua&logoColor=white) ![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white) ![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)

In order to use ESX Legacy you will need a database wrapper first. You can choose between

* [Oxmysql](https://github.com/overextended/oxmysql/) | newer and more recent, but requires query updating.
* [MySQL-Async](https://github.com/brouznouf/fivem-mysql-async) | which is outdated.


Since ESX Legacy, there is no longer need to use the following:



Client side
```
ESX = nil

Citizen.CreateThread(function()
  while ESX == nil do
	TriggerEvent('esx:getSharedObject', function(obj) ESX = obj end)
	   Citizen.Wait(1)
	end
end)
```

Server side

```
ESX = nil

TriggerEvent('esx:getSharedObject', function(obj) ESX = obj end)
```

You can simply import functionality by using this inside of your fxmanifest.lua

```
shared_script '@es_extended/imports.lua'
``` 


---
License
ESX Legacy - Roleplay Framework for FiveM

Originally created by Jérémie N'gadi


This program Is free software: you can redistribute it And/Or modify it under the terms Of the GNU General Public License As published by the Free Software Foundation, either version 3 Of the License, Or (at your option) any later version.

This program Is distributed In the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty Of MERCHANTABILITY Or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License For more details.

You should have received a copy Of the GNU General Public License along with this program. If Not, see http://www.gnu.org/licenses/.

Copyright (C) 2015-2022 Jérémie N'gadi
