# Setup routes in Ruby on Rails

When setting up routes the priority is based upon the order of creation. The first created route has the highest priority.  
You can view how all your routes are layed out using `rake routes`.  

Having root of your site routed with "root":  
`root 'controller#action'`    

**Example**  
`root 'static#home'`

## Routing to static pages

This routes are defined with simple, unparametized rules.  
`Syntax: 'path', to: 'controller#action'`  

**Example**:  
```
get '/help',    to:   'static#help'
get '/about',   to:   'static#about'
get '/contact', to:   'static#contact'
```
