### Info

This is a small NSView subclass that accepts file drag & drop and is easy to setup. It is currently being used in [MacSymbolicator](http://mahdi.jp/apps/macsymbolicator). It can probably be done much easier and with cleaner code (I am not proud), it was an experiment and I've learned so much since then.

Hope it's useful to you.

![](http://i.imgur.com/hETOuJn.png)
![](http://i.imgur.com/0IEt9bE.png)

### Usage

	- (void)setupDropzone {
		MBDropZone* dropzone = [][MBDropZone alloc] initWithFrame:CGRectMake(0, 0, 200, 200)];
	    dropzone.text = @"Drop Crash Report"; 
	    dropzone.fileType = @".crash"; // Sets the icon and file type it accepts
	    dropzone.delegate = self;
	}
	
	- (void)dropZone:(MBDropZone*)dropZone receivedFile:(NSString*)file {
		NSLog(@"User dropped '%@'", file);
	}
    
    
    