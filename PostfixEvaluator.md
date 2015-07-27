# Postfix Evaluator
```ruby
  class PostfixEvaluator

  def initialize(postfix)
    @postfix = postfix
  end


  def compute
    OPERATORS = ['+', '-', '/', '*']

    stack = []
    operators = []
    numbers = []

    stack = @postfix.reverse.split(' ')
    
    begin   
      top = stack.pop       

      if OPERATORS.include?(top)
        operators.push(top)
      else
        numbers.push(top)
      end

      if numbers.length >= 2 && operators.length > 0
        num1 = numbers.pop.to_i
        num2 = numbers.pop.to_i
        op = operators.pop

        if op == "+"
                    value = num1 + num2
                elsif op == "-"
                    value = num1 - num2
                elsif op == "/"
                    value = num1 / num2
                elsif op == "*"
                    value = num1 * num2
                end

                numbers.push(value)
                                
      end

    end while stack.length > 0

    return 'Invalid Postfix Notation' if numbers.length > 1 || operators.length > 0
        puts numbers
  end
end

evaluator = PostfixEvaluator.new '3 4 + 5 *'
evaluator.compute
```
