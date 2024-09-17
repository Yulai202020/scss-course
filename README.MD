# Variables

```scss
$variable_name: value;
@debug $variable_name;
```

# For, Each, While

### for

```scss
@for $i from 1 through 10 { // var i goes from 1 to 10
    @debug $1;
}
```

### each

```scss
$some_list: 1, 2, 3, 4, 5;
@each $element in $some_list {
    @debug $some_list;
}
```

### while

```scss
$i: 1;
@while {
    @debug $i;
    $i: $i + 1;
}
```

# Imports: @use @import

### @import old version

```scss
@import 'path/to/file';
```

Its add code of 'path/to/file' to your files.

### @use modern version
```scss
@use 'path/to/file' as module;
```

Its adds to var module anythink from file 'path/to/file', or:

```scss
@use 'path/to/file'; // its work same as @import
```

# forward exporting for @use

```scss
```

# Others @error @warn @debug

This things work just on compilation,
if you need to print smth on compilation you do:

```scss
@debug "somethink";
```

if you need to warn yourself:

```scss
@warn "here can be bug!";
```

if somethink heppen and its cloud not heppen you throw error:

```scss
@error "critical error!!!";
```