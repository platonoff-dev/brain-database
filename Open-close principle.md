### Open Close principles
This means that i should be able to add new functionality without changing my existing code structures, but by adding new code instead.

Example:
```python
class Album:  
    def __init__(self, name, artist, songs, genre):  
        self.name = name  
        self.artist = artist  
        self.songs = songs  
        self.genre = genre#before  

class AlbumBrowser:  
    def search_album_by_artist(self, albums, artist):  
        return [album for album in albums if album.artist == artist] def 
	
	def search_album_by_genre(self, albums, genre):  
        return [album for album in albums if album.genre == genre]
```


So, If i need to search by artist and and genre wee need to create new method. I think it is bad solution.
 ```python
 class SearchBy:  
    def is_matched(self, album):  
        pass  
        
class SearchByGenre(SearchBy):  
    def __init__(self, genre):  
        self.genre = genre def is_matched(self, album):  
        return album.genre == self.genre  
      
class SearchByArtist(SearchBy):  
    def __init__(self, artist):  
        self.artist = artist def is_matched(self, album):  
        return album.artist == self.artist  
      
class AlbumBrowser:  
    def browse(self, albums, searchby):  
        return [album for album in albums if searchby.is_matched(album)]
 
 ```
