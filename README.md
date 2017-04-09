# colorful

Terminal string styling done right, in Python :tada:

## Here's a tease

```python
import colorful

# create a colored string using clever method translation
print(colorful.bold_white('Hello World'))
# create a colored string using `str.format()`
print('{c.bold}{c.black_on_white}Hello World{c.reset}'.format(c=colorful))

# choose specific color mode for one block
with colorful.use_true_colors() as c:
    print(c.lightCoral('colorful is awesome!'))
    
# choose specific style for color names
with colorful.use_style('solarized') as c:
    # print the official solarized colors
    print(c.yellow('yellow'), c.orange('orange'), c.red('red'), c.magenta('magenta'), 
        c.violet('violet'), c.blue('blue') c.cyan('cyan'), c.green('green'))
        
# create and choose your own color palette
MY_COMPANY_PALETTE = {
    'companyOrange': '#f4b942',
    'companyBaige': '#e8dcc5'
}
with colorful.use_palette(my_company_palette) as c:
    print(c.companyOrange_on_companyBaige('Thanks for choosing our product!'))
```

***

*<p align="center">This project is published under [MIT](LICENSE).<br>A [Timo Furrer](https://tuxtimo.me) project.<br>- :tada: -</p>*
