## Block a.k.a Grid

The blocks use html flexbox. There are two types of blocks that we use for the dashboard, **row** and **block**.


The container is called **container** and it is a class. The **container** should be the root html element since it has the flexbox properties.
This is how the html code for the **container** looks like :

```html
<div class='container'>
...
</div>
```
#### Full row
Full row will take 100% of the container.
This is how the html code for the **row** looks like :
```html
<div class='row'>
..
</div>
```
**Full row all together**
```html
<div class='container'>
    <div class='row'>
    ...
    </div>
</div>
```
#### Split row into blocks
If you want to to split the row into to blocks you can do so by adding the block class. The block will be split equally so for example :

if you have 1 block in a row it will be 100%.
If you have 2 blocks in a row they will be 50% each.
if you have 3 blocks in a row they will be 33% each.
if you have 4 blocks in a row they will be 25% each

and so on, you get the point.
```html
<div class='container'>
    <div class='row'>
        <div class='block'>
        ...
        </div>
        <div class='block'>
        ...
        </div>
    </div>
</div>
```

##### what about nesting ?

If you want to nest the blocks you can do so by doing like this (you can nest unlimited times):

```html
<div class='container'>
    <div class='row'>
        <div class='block'>
            <div class='row'>
                <div class='block'>
                ...
                </div>
                <div class='block'>
                ...
                </div>
            </div>
        </div>
        <div class='block'>
        ...
        </div>
    </div>
</div>
```

#### What if you dont want each block to always be 50% ?
Lets say that you want a naviagation on the left and the content on the right
so that it will be 25% for the navigation and 75% for the content.
The only thing that you need to do is add a class to the blocks that you want to split.

So if we would make the navigation and the content blocks we will do it like this :
```html
        <div class='container'>
          <div class='row'>
            <div class='block'>
              <div class='border'>
                <div class='content'>
                  <div class='row'>
                    <div class='block _25'>
                      Navigation
                    </div>
                    <div class='block _75'>
                      Content
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
```

The blocks must be 100% combined inside each row to get the correct structure. You can split up the row how many times you want as long as the combined blocks are 100%.
The classes that you can use are :

| Class name        | Propertie     |
| :-------------    | :-------------|
| _5                | 5%            |
| _10               | 10%           |
| _15               | 15%           |
| _20               | 20%           |
| _25               | 25%           |
| _30               | 30%           |
| _35               | 35%           |
| _40               | 40%           |
| _45               | 45%           |
| _50               | 50%           |
| _55               | 55%           |
| _60               | 60%           |
| _65               | 65%           |
| _70               | 70%           |
| _75               | 75%           |
| _80               | 80%           |
| _85               | 85%           |
| _90               | 90%           |
| _95               | 95%           |
| _100              | 100%          |



## Styling
#### Style the blocks
**Important**
Don't ever add class to the container,row or block. Since we are using a styling for the blocks we have to add the border like this


This is how it will look on a **block** :

```html
        <div class='container'>
          <div class='row'>
            <div class='block'>
              <div class='border'>
                  <div class='content'>
                    100% full block
                  </div>
              </div>
            </div>
          </div>
        </div>
```
And this is how it will look with **2 blocks** :

```html
        <div class='container'>
          <div class='row'>
            <div class='block'>
              <div class='border'>
                  <div class='content'>
                    100% full block
                  </div>
              </div>
            </div>
            <div class='block'>
              <div class='border'>
                  <div class='content'>
                    100% full block
                  </div>
              </div>
            </div>
          </div>
        </div>
```




---
#### Written by **Cyrus Zei** 2017-01-18
