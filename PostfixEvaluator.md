# Postfix Evaluator
```ruby
  class PostfixEvaluator
  	def initialize(postfix)
  		@postfix = postfix
  	end
  
  	def compute
  		stack = @postfix.split(' ').reverse
  
  		until stack.length == 1
  
  			if stack.length < 3
  				puts "Invalid Postfix Notation"
  				break
  			else
  				num1 = stack.pop
  				num2 = stack.pop
  				operand = stack.pop
  				value = 0
  
  				if num1 == "+" || num1 == "-" || num1 == "/" || num1 == "*" || num2 == "+" || num2 == "-" || num2 == "/" || num2 == "*" 
  					puts "Invalid Postfix Notation"
  					break
  				end
  
  				if operand == "+"
  					value = num1.to_i + num2.to_i
  				elsif operand == "-"
  					value = num1.to_i - num2.to_i
  				elsif operand == "/"
  					value = num1.to_i / num2.to_i
  				elsif operand == "*"
  					value = num1.to_i * num2.to_i
  				else
  					puts "Invalid Postfix Notation"
  					break
  				end
  
  				if stack.length==0
  					puts value.to_s
  					break
  				else
  					stack.push(value.to_s)
  				end				
  			end
  		end
  	end
  end
  
  evaluator = PostfixEvaluator.new '3 4 + 5 *'
  evaluator.compute
```
