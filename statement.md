# Bonjour
  
  Chuck Norris a un clavier avec seulement deux touches.
  Le 0 et la barre d'espacement lui suffisent pour envoyer un message.
  
  
```ruby runnable
# Cette version est codée par moi : 
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
# et voici la version codée par Chuck Norris :
  
```ruby runnable
puts "Entrez votre phrase à coder en unaire ici ".chomp.bytes.map{|b|'%07b'%b}.join.chars.chunk{|e|e}.flat_map{|k,v|[['00','0'][k.to_i],'0'*v.size]}*' '
```  
# Merci codingame.com

                                          MMMMMMMMMMM
                                       MMMMMMMMMMMMMMMMM
                                   NMMMMMMMMMMMMMMMMMMMMMMMM
                                 MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM
                                MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMN
                                MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM
                                MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM
                               MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMD
                              DMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM
                              MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM
                              MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM
                             MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM
                             MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM
                            MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMN
                            MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMN
                           MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMN
                           MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMN
      NM                  MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM
      MMMMM              MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM
       MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM
        MMMMMMMMMMMMMMMMMMMMMMMMMM8MMMMMMMMMIMMMMM8,. ...........OMMMMMMMMMMMMMMMMMMMMMMMMMMMM
           MMMMMMMMMMMMMMMMMMMMMMM ..N. .....~MMMM...............:MMMMNMMMMMMMMMMMMMMMMMMMMMMM
             NMMMMMMMMMMMMMMMMMMMMM.....:..DMMMMMNZ Z.... .......M$MMMMMMMMMMMMMMMMMMMMMMMMMMM
                 MMMMMMMMMMNMMMMMMM....... 7=MMMMMMO....Z .......MM7MMMMMMMMMMMMMMMMMMMMMMMMM
                    MMMMMMMMMMMMMMMMM  Z...MMMZ .. .,M..,........MMMMMMMMMMMMMMMMMMMMMMMMMMMM
                        MMMMMM.......DOM ....N7..................MMMMMMMMMMMMMMMMMMMMMMMMMMM
                           MMM....... M. ... .  ... ..............M...$MMMMMMMMMMMMMMMMMMMM
                             ........... ........~. ..............M..=....+MMMMMMMMMMMMMM
                             ......+.NMI~........ . ..............M.,.I...MMMMMMMMMMMMMMN
                             ......$... ...... O..................,.....$MMMMMMMMMMMMN
                             .....M.......... M M.. .............. 8  .OMMMMMMMMMMMN
                              ..=7I,,.,,IMI...M.................. ..MMMMMMMMMMM
                              ....DMMMMMMMMMMMMMMMO..............D...MMMMMMMMM
                               .MMMMMMMMMMMMMMDDMM:,N..............DMMMMMMMMMMM
                               NMMMMMNMM8 . .... ...,~............  MMMMMMMMM
                               MMMMM,:......::~..M8M8MM...............MMMMMM
                               MMMM ... . .........,MM..............MMMMMO$
                               MMMMM... =.=. .. . . MM ....... . ...MMMMMMM
                                NMMMMMMMMMM?  ..O.?NM7 ....... ......MMMMMM
                                 NMMMMMMMMMMMMMMMMM........  $ . ...MMMNMMM
                                  MMMMMMMMMMMMMMM.........,, ......MMMMMMMM
                                   OMMMMMMMM8 , .. .. .,N.... ...:MMMMMMMMMMN
                                    MMMMMMMM?N. ...~MD.:MNI8MMMMMMMMMMMMMMMMMN
                               MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMN
                            NMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMN
                           MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMN
                        MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM
                     MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM
                    NMMMMMMMMMMMMNMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM
                   MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM
