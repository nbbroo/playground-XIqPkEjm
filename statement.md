# Bonjour
  
  Chuck Norris a un clavier à deux touches le 0 et la barre d'espacement.
  Cela lui suffit emplement pour envoyer un message.
  
```ruby runnable

@myStr = "Entrez votre phrase à coder en unaire ici "

@myStr = @myStr.reverse
myStrLength = @myStr.length

@myStrB = ""

@anser = nil.to_s
@compter = 0
@myStrB = @myStrB += @myStr.unpack('b7'* myStrLength).to_s.reverse

@myStrB.gsub!('"','')
@myStrB.gsub!(' ','')
@myStrB.gsub!('[','')
@myStrB.gsub!(']','')
@myStrB.gsub!(',','')
@myStrB.downcase

@compter = 0

while @myStrB.length != 0 
    @current = @myStrB[0] 
    @current == "1" ? @anser << "0 " : @anser << "00 " 

    for i in 0..@myStrB.length
    @current == @myStrB[i] ? @compter += 1 : break
    end

    for i in 1..@compter
    @anser << "0"
    @myStrB = @myStrB.reverse.chop.reverse
    end

@anser << " "
@compter = 0
end 

 puts @anser.chop
 
```

# Merci codingame.com

