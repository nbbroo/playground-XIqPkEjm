# Bonjour
  
  Chuck Norris a un clavier avec seulement deux touches.
  Le 0 et la barre d'espacement lui suffisent pour envoyer un message.
  Cette version est codée par moi : 
  
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

# et voici la version codé par Chuck Norris :
  
```ruby runnable
@myStr = "Entrez votre phrase à coder en unaire ici "
puts @myStr.chomp.bytes.map{|b|'%07b'%b}.join.chars.chunk{|e|e}.flat_map{|k,v|[['00','0'][k.to_i],'0'*v.size]}*' '

```  
# Merci codingame.com
