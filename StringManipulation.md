# First Implementation
```ruby
  def join_string(string1, string2)

  	# First approach using + operator
  	puts string1 + ' ' + string2
  
  end
  
  string1 = 'Hello'
  string2 = 'World'
  
  join_string(string1, string2)
```

# Second Implementation
```ruby
  def join_string(string1, string2)
  
  	# Second approach using prepend() method
  	puts string2.prepend(' '.prepend(string1))
  	
  end
  
  string1 = 'Hello'
  string2 = 'World'
  
  join_string(string1, string2)
```
