# DiagramaDeClasse
Diagrama de Classe do Iphone
---
config:
  class:
    hideEmptyMembersBox: true
---
classDiagram
direction TB
    class Player {
	    play()
	    stop()
	    back()
	    next()
    }
    class PlayerMusic {
	    Int numFaixa
	    String nameAlbum
	    String nameMusic
	    play()
	    pause()
	    back()
	    next()
	    selectMusic()
    }
    class PlayerVideo {
	    String nameVideo
	    pause()
	    play()
	    back()
	    next()
	    selectVideo()
    }
    class Iphone {
    }
    class Call {
	    String num
	    call()
	    send()
    }
    class Browser {
	    String url
	    displayPage()
	    addTab()
    }

	<<Classe>> PlayerMusic
	<<Classe>> PlayerVideo
	<<Classe>> Iphone
	<<Class>> Call
	<<Class>> Browser

    Player -- PlayerMusic
    Player -- PlayerVideo
    Iphone -- Player
    Iphone -- Call
    Iphone -- Browser
