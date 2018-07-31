# Ruby-Project1
Booking a Hotel 

puts
puts
puts "\t\t*********************************************************"
puts "\t\t*\t\t\tWelcome!\t\t\t*"
puts "\t\t*\t\t     Please select\t\t\t*"
puts "\t\t*\t\t\tHotel:\t\t\t\t*"
puts "\t\t* - - - - - - - - - - - - - - - - - - - - - - - - - - - *"

puts "\t\t*    A. The Grand   $200/night    $500 for 3 nights\t*"
puts "\t\t*    B. The Ritz    $250 per night   \t\t\t*"
puts "\t\t*    C. Fairmont    $300/night    $700 for 3 nights\t*"
puts "\t\t*    D. Rosewood    $500 per night   \t\t\t*"
puts "\t\t*********************************************************"

a=0
b=0
c=0
d=0

aCost=0
bCost=0
cCost=0
dCost=0

puts "Which hotel?"
answer = gets.chomp.upcase
loop do
if answer=='A'||answer=='B'||answer=='C'||answer=='D'
 puts 'For how many nights?'
 num=gets.chomp.to_i
     if answer=="A"
         a=num
        
     elsif answer=="B"
         b=num
        
     elsif answer=="C"
         c=num
        
     elsif answer=="D"
         d=num
        
     end
 else
 break
 end
puts 'any other hotels?'
answer=gets.chomp.upcase
end

aCost = (a/3)*500 + (a%3)*200 

bCost = 250*b 

cCost = (c/3)*700 + (c%3)*300

dCost=500*d

totalCost=aCost+bCost+cCost+dCost



puts "You are staying at The Grand for " + a.to_s + " nights for a total cost of $" + aCost.to_s
puts "You are staying at The Ritz for " + b.to_s + " nights for a total cost of $" + bCost.to_s
puts "You are staying at The Fairmont for " + c.to_s + " nights for a total cost of $" + cCost.to_s
puts "You are staying at The Rosewood for " + d.to_s + " nights for a total cost of $" + dCost.to_s
puts 
puts "Your Grand Total is $" + totalCost.to_s
