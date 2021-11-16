# require.lua
Require all files in a folder

### Credit

Written by [@kikito](https://github.com/kikito) and published in [love forums](https://love2d.org/forums/viewtopic.php?p=102281#p102281) under MIT license. Updated to work with newer love2d versions.


> Post by kikito » Fri May 10, 2013 8:00 am
> 
> I did this some time ago:
> 
> https://github.com/kikito/fay/blob/master/src/lib/require.lua
> 
> It extends require with some methods. 

### Usage

> The usage for requiring the files in a folder is:

```lua
require 'require' -- or require 'lib.require', depending on where you put it
local d = require.tree('path.to.directory')
d.file1 -- contents returned by path/to/directory/file1.lua
d.file2 -- contents returned by path/to/directory/file2.lua
d.subdir.file3 -- contents returned by path/to/directory/subdir/file3.lua
```
> As a bonus, you also have require.relative:
```lua
local f = require.relative(..., "hello") -- if the path to the current file is 'foo.bar.baz', this requires 'foo.bar.hello'
```
> Note that `require('file')` without methods works exactly like before.
