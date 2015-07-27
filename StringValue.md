# String Value
```ruby
  class StringValue
  	def initialize(convert)
  		@string_to_convert = convert
  	end
  
  	def compute
  		alphabet_hash = Hash.new
  		alphabet = 'A'	
  		for i in 1..26 do
  			alphabet_hash[alphabet] = i
  			alphabet = alphabet.next
  		end
  
  		sum = 0
  		string_array = @string_to_convert.split('')
  		string_array.each do |key|
  			if alphabet_hash.has_key?(key)
  				sum = alphabet_hash[key] + sum	
  			else 
  				sum = 0 + sum
  			end
  		end
  		
  		puts sum
  	end
  end
  
  my_class = StringValue.new 'HELLO'
  my_class.compute
```
