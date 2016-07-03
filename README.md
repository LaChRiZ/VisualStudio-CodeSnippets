# Code snippets for Visual Studio


## Snippets


### Visual C# #

* `cr` - Console.Readline() snippet.

* `#ctor` - Constructor with sourrounding region.

* `inpc` - Implementation of INotifyPropertyChanged interface.

* `#region` - Region with comment at the endregion mark.

* `property` - Property with hidden field that raises PropertyChanged event.

* `sf` - String.Format("") snippet.

* `tostr` - Implements ToString() method.

* `tostrf` - Implements ToString() method by use of String.Format();

---

## Implementations

### Visual C&#35; implementations

* `cr`  
```c#
    Console.Readline();
```

* `#ctor`  
```c#
    #region Constructors

    public Class ()
    {
    }

    #endregion // Constructors
```

* `inpc`  
```c#
    #region INotifyPropertyChanged Members
        
    /// <summary>
    /// Raised, when a property value changed.
    /// </summary>
    public event PropertyChangedEventHandler PropertyChanged;

    /// <summary>
    /// Raises <see cref="PropertyChanged"/>-Event.
    /// </summary>
    /// <param name="propertyName">Name of the property that has updated</param>
    protected void OnPropertyChanged([CallerMemberName] string propertyName = "")
    {
        PropertyChanged?.Invoke(this, new PropertyChangedEventArgs(propertyName));
    }

    #endregion // INotifyPropertyChanged Members
```

* `#region`  
```c#
    #region YourRegion
		
	#endregion // YourRegion
```

* `property`  
```c#
    private object _value;

        public object Value
        {
            get { return _value; }
            set
            {
                _value = value;
                OnPropertyChanged("Value);
            }
        }
```

* `sf`  
```c#
    string.Format("foo")
```

* `tostr`  
```c#
    /// <summary>
    /// Returns your Object as string.
    /// </summary>
    /// <returns>String representation of your Object.</returns>
    public override string ToString()
    {
        return base.ToString();
    }
```

* `tostrf`  
```c#
    /// <summary>
    /// Returns your Object as string.
    /// </summary>
    /// <returns>String representation of your Object.</returns>
    public override string ToString()
    {
        return string.Format("{0}", this.GetType());
    }
```


---

## How to install

1. Clone or download repository.

2. Copy all files (including directories), or just these snippets, you want to use, in your Visual Studio code snippets folder.

    * If you use VS 2015: [C:\\Users\\%USERNAME%\\Documents\\Visual Studio 2015\\Code Snippets](C:\Users\%USERNAME%\Documents\Visual Studio 2015\Code Snippets)

3. Start Visual Studio. If it's already running, restart is not necessary.


---
(in german/auf deutsch)


## Installationsanleitung

1. Klone das Repository oder lade es herunter.

2. Kopiere alle Dateien (inklusive der Verzeichnisse), oder einfach nur die Code-Snippets, die du nutzen willst, in deinen Visual Studio Code-Snippets-Ordner.

3. Starte Visual Studio. Wenn es bereits läuft, ist kein Neustart erforderlich.
