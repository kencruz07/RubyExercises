# First Implementation

```ruby
  def multiply(multiplicand, multiplier)
  	sum = 0
  
  	First approach using Integer.times operator
  	multiplier.times do
  		 sum = multiplicand + sum
  	end
  	puts sum
  	
  end
  
  multiplicand = 4
  multiplier = 5
  
  multiply(multiplicand, multiplier)
```

# Second Implementation
```ruby
  def multiply(multiplicand, multiplier)
  	sum = 0
  
    # Second approach using while loop
  	i = 0
  	while i < multiplier  do
  		sum = multiplicand + sum
  	    i+=1
  	end
  	puts sum
  	
  end
  
  multiplicand = 4
  multiplier = 5
  
  multiply(multiplicand, multiplier)
```
