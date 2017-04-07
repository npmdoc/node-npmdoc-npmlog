# api documentation for  [npmlog (v4.0.2)](https://github.com/npm/npmlog#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-npmlog.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-npmlog) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-npmlog.svg)](https://travis-ci.org/npmdoc/node-npmdoc-npmlog)
#### logger for npm

[![NPM](https://nodei.co/npm/npmlog.png?downloads=true)](https://www.npmjs.com/package/npmlog)

[![apidoc](https://npmdoc.github.io/node-npmdoc-npmlog/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-npmlog_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-npmlog/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-npmlog/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-npmlog/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Isaac Z. Schlueter",
        "email": "i@izs.me",
        "url": "http://blog.izs.me/"
    },
    "bugs": {
        "url": "https://github.com/npm/npmlog/issues"
    },
    "dependencies": {
        "are-we-there-yet": "~1.1.2",
        "console-control-strings": "~1.1.0",
        "gauge": "~2.7.1",
        "set-blocking": "~2.0.0"
    },
    "description": "logger for npm",
    "devDependencies": {
        "standard": "~7.1.2",
        "tap": "~5.7.0"
    },
    "directories": {},
    "dist": {
        "shasum": "d03950e0e78ce1527ba26d2a7592e9348ac3e75f",
        "tarball": "https://registry.npmjs.org/npmlog/-/npmlog-4.0.2.tgz"
    },
    "files": [
        "log.js"
    ],
    "gitHead": "a3b7aed07790b674aa1fecfc81a61481abeaf882",
    "homepage": "https://github.com/npm/npmlog#readme",
    "license": "ISC",
    "main": "log.js",
    "maintainers": [
        {
            "name": "iarna",
            "email": "me@re-becca.org"
        },
        {
            "name": "isaacs",
            "email": "i@izs.me"
        },
        {
            "name": "othiym23",
            "email": "ogd@aoaioxxysz.net"
        },
        {
            "name": "zkat",
            "email": "kat@sykosomatic.org"
        }
    ],
    "name": "npmlog",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/npm/npmlog.git"
    },
    "scripts": {
        "test": "standard && tap test/*.js"
    },
    "version": "4.0.2"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module npmlog](#apidoc.module.npmlog)
1.  boolean <span class="apidocSignatureSpan">npmlog.</span>progressEnabled
1.  [function <span class="apidocSignatureSpan">npmlog.</span>_format (msg, style)](#apidoc.element.npmlog._format)
1.  [function <span class="apidocSignatureSpan">npmlog.</span>addLevel (lvl, n, style, disp)](#apidoc.element.npmlog.addLevel)
1.  [function <span class="apidocSignatureSpan">npmlog.</span>clearProgress (cb)](#apidoc.element.npmlog.clearProgress)
1.  [function <span class="apidocSignatureSpan">npmlog.</span>disableColor ()](#apidoc.element.npmlog.disableColor)
1.  [function <span class="apidocSignatureSpan">npmlog.</span>disableProgress ()](#apidoc.element.npmlog.disableProgress)
1.  [function <span class="apidocSignatureSpan">npmlog.</span>disableUnicode ()](#apidoc.element.npmlog.disableUnicode)
1.  [function <span class="apidocSignatureSpan">npmlog.</span>emitLog (m)](#apidoc.element.npmlog.emitLog)
1.  [function <span class="apidocSignatureSpan">npmlog.</span>enableColor ()](#apidoc.element.npmlog.enableColor)
1.  [function <span class="apidocSignatureSpan">npmlog.</span>enableProgress ()](#apidoc.element.npmlog.enableProgress)
1.  [function <span class="apidocSignatureSpan">npmlog.</span>enableUnicode ()](#apidoc.element.npmlog.enableUnicode)
1.  [function <span class="apidocSignatureSpan">npmlog.</span>error ()](#apidoc.element.npmlog.error)
1.  [function <span class="apidocSignatureSpan">npmlog.</span>gauge._themes (opts)](#apidoc.element.npmlog.gauge._themes)
1.  [function <span class="apidocSignatureSpan">npmlog.</span>http ()](#apidoc.element.npmlog.http)
1.  [function <span class="apidocSignatureSpan">npmlog.</span>info ()](#apidoc.element.npmlog.info)
1.  [function <span class="apidocSignatureSpan">npmlog.</span>log ()](#apidoc.element.npmlog.log)
1.  [function <span class="apidocSignatureSpan">npmlog.</span>newGroup ()](#apidoc.element.npmlog.newGroup)
1.  [function <span class="apidocSignatureSpan">npmlog.</span>newItem ()](#apidoc.element.npmlog.newItem)
1.  [function <span class="apidocSignatureSpan">npmlog.</span>newStream ()](#apidoc.element.npmlog.newStream)
1.  [function <span class="apidocSignatureSpan">npmlog.</span>pause ()](#apidoc.element.npmlog.pause)
1.  [function <span class="apidocSignatureSpan">npmlog.</span>resume ()](#apidoc.element.npmlog.resume)
1.  [function <span class="apidocSignatureSpan">npmlog.</span>setGaugeTemplate (template)](#apidoc.element.npmlog.setGaugeTemplate)
1.  [function <span class="apidocSignatureSpan">npmlog.</span>setGaugeThemeset (themes)](#apidoc.element.npmlog.setGaugeThemeset)
1.  [function <span class="apidocSignatureSpan">npmlog.</span>showProgress ()](#apidoc.element.npmlog.showProgress)
1.  [function <span class="apidocSignatureSpan">npmlog.</span>silent ()](#apidoc.element.npmlog.silent)
1.  [function <span class="apidocSignatureSpan">npmlog.</span>silly ()](#apidoc.element.npmlog.silly)
1.  [function <span class="apidocSignatureSpan">npmlog.</span>useColor ()](#apidoc.element.npmlog.useColor)
1.  [function <span class="apidocSignatureSpan">npmlog.</span>verbose ()](#apidoc.element.npmlog.verbose)
1.  [function <span class="apidocSignatureSpan">npmlog.</span>warn ()](#apidoc.element.npmlog.warn)
1.  [function <span class="apidocSignatureSpan">npmlog.</span>write (msg, style)](#apidoc.element.npmlog.write)
1.  number <span class="apidocSignatureSpan">npmlog.</span>_eventsCount
1.  number <span class="apidocSignatureSpan">npmlog.</span>maxRecordSize
1.  object <span class="apidocSignatureSpan">npmlog.</span>_buffer
1.  object <span class="apidocSignatureSpan">npmlog.</span>_events
1.  object <span class="apidocSignatureSpan">npmlog.</span>disp
1.  object <span class="apidocSignatureSpan">npmlog.</span>domain
1.  object <span class="apidocSignatureSpan">npmlog.</span>gauge
1.  object <span class="apidocSignatureSpan">npmlog.</span>gauge._tty
1.  object <span class="apidocSignatureSpan">npmlog.</span>gauge._writeTo
1.  object <span class="apidocSignatureSpan">npmlog.</span>headingStyle
1.  object <span class="apidocSignatureSpan">npmlog.</span>levels
1.  object <span class="apidocSignatureSpan">npmlog.</span>prefixStyle
1.  object <span class="apidocSignatureSpan">npmlog.</span>record
1.  object <span class="apidocSignatureSpan">npmlog.</span>style
1.  object <span class="apidocSignatureSpan">npmlog.</span>tracker
1.  string <span class="apidocSignatureSpan">npmlog.</span>level

#### [module npmlog._events](#apidoc.module.npmlog._events)
1.  [function <span class="apidocSignatureSpan">npmlog._events.</span>error ()](#apidoc.element.npmlog._events.error)

#### [module npmlog.gauge](#apidoc.module.npmlog.gauge)
1.  boolean <span class="apidocSignatureSpan">npmlog.gauge.</span>_cleanupOnExit
1.  boolean <span class="apidocSignatureSpan">npmlog.gauge.</span>_disabled
1.  boolean <span class="apidocSignatureSpan">npmlog.gauge.</span>_fixedFramerate
1.  boolean <span class="apidocSignatureSpan">npmlog.gauge.</span>_hideCursor
1.  boolean <span class="apidocSignatureSpan">npmlog.gauge.</span>_needsRedraw
1.  boolean <span class="apidocSignatureSpan">npmlog.gauge.</span>_onScreen
1.  boolean <span class="apidocSignatureSpan">npmlog.gauge.</span>_paused
1.  boolean <span class="apidocSignatureSpan">npmlog.gauge.</span>_showing
1.  [function <span class="apidocSignatureSpan">npmlog.gauge.</span>_themes (opts)](#apidoc.element.npmlog.gauge._themes)
1.  number <span class="apidocSignatureSpan">npmlog.gauge.</span>_updateInterval
1.  object <span class="apidocSignatureSpan">npmlog.gauge.</span>_gauge
1.  object <span class="apidocSignatureSpan">npmlog.gauge.</span>_lastUpdateAt
1.  object <span class="apidocSignatureSpan">npmlog.gauge.</span>_removeOnExit
1.  object <span class="apidocSignatureSpan">npmlog.gauge.</span>_status
1.  object <span class="apidocSignatureSpan">npmlog.gauge.</span>_theme
1.  object <span class="apidocSignatureSpan">npmlog.gauge.</span>_tty
1.  object <span class="apidocSignatureSpan">npmlog.gauge.</span>_writeTo

#### [module npmlog.gauge._themes](#apidoc.module.npmlog.gauge._themes)
1.  [function <span class="apidocSignatureSpan">npmlog.gauge.</span>_themes (opts)](#apidoc.element.npmlog.gauge._themes._themes)
1.  [function <span class="apidocSignatureSpan">npmlog.gauge._themes.</span>addTheme (name, parent, theme)](#apidoc.element.npmlog.gauge._themes.addTheme)
1.  [function <span class="apidocSignatureSpan">npmlog.gauge._themes.</span>addToAllThemes (theme)](#apidoc.element.npmlog.gauge._themes.addToAllThemes)
1.  [function <span class="apidocSignatureSpan">npmlog.gauge._themes.</span>getDefault (opts)](#apidoc.element.npmlog.gauge._themes.getDefault)
1.  [function <span class="apidocSignatureSpan">npmlog.gauge._themes.</span>getTheme (name)](#apidoc.element.npmlog.gauge._themes.getTheme)
1.  [function <span class="apidocSignatureSpan">npmlog.gauge._themes.</span>getThemeNames ()](#apidoc.element.npmlog.gauge._themes.getThemeNames)
1.  [function <span class="apidocSignatureSpan">npmlog.gauge._themes.</span>newMissingDefaultThemeError (platformName, hasUnicode, hasColor)](#apidoc.element.npmlog.gauge._themes.newMissingDefaultThemeError)
1.  [function <span class="apidocSignatureSpan">npmlog.gauge._themes.</span>newMissingThemeError (name)](#apidoc.element.npmlog.gauge._themes.newMissingThemeError)
1.  [function <span class="apidocSignatureSpan">npmlog.gauge._themes.</span>newTheme (parent, theme)](#apidoc.element.npmlog.gauge._themes.newTheme)
1.  [function <span class="apidocSignatureSpan">npmlog.gauge._themes.</span>newThemeSet ()](#apidoc.element.npmlog.gauge._themes.newThemeSet)
1.  [function <span class="apidocSignatureSpan">npmlog.gauge._themes.</span>setDefault (opts, name)](#apidoc.element.npmlog.gauge._themes.setDefault)
1.  object <span class="apidocSignatureSpan">npmlog.gauge._themes.</span>baseTheme
1.  object <span class="apidocSignatureSpan">npmlog.gauge._themes.</span>defaults
1.  object <span class="apidocSignatureSpan">npmlog.gauge._themes.</span>themes

#### [module npmlog.gauge._tty](#apidoc.module.npmlog.gauge._tty)
1.  boolean <span class="apidocSignatureSpan">npmlog.gauge._tty.</span>_hadError
1.  boolean <span class="apidocSignatureSpan">npmlog.gauge._tty.</span>_isStdio
1.  boolean <span class="apidocSignatureSpan">npmlog.gauge._tty.</span>allowHalfOpen
1.  boolean <span class="apidocSignatureSpan">npmlog.gauge._tty.</span>connecting
1.  boolean <span class="apidocSignatureSpan">npmlog.gauge._tty.</span>destroyed
1.  boolean <span class="apidocSignatureSpan">npmlog.gauge._tty.</span>readable
1.  boolean <span class="apidocSignatureSpan">npmlog.gauge._tty.</span>writable
1.  [function <span class="apidocSignatureSpan">npmlog.gauge._tty.</span>_write (chunk, encoding, callback)](#apidoc.element.npmlog.gauge._tty._write)
1.  [function <span class="apidocSignatureSpan">npmlog.gauge._tty.</span>_writeDefault (data, encoding, cb)](#apidoc.element.npmlog.gauge._tty._writeDefault)
1.  [function <span class="apidocSignatureSpan">npmlog.gauge._tty.</span>destroy (er)](#apidoc.element.npmlog.gauge._tty.destroy)
1.  [function <span class="apidocSignatureSpan">npmlog.gauge._tty.</span>destroySoon (er)](#apidoc.element.npmlog.gauge._tty.destroySoon)
1.  number <span class="apidocSignatureSpan">npmlog.gauge._tty.</span>_bytesDispatched
1.  number <span class="apidocSignatureSpan">npmlog.gauge._tty.</span>_eventsCount
1.  number <span class="apidocSignatureSpan">npmlog.gauge._tty.</span>columns
1.  number <span class="apidocSignatureSpan">npmlog.gauge._tty.</span>fd
1.  number <span class="apidocSignatureSpan">npmlog.gauge._tty.</span>rows
1.  object <span class="apidocSignatureSpan">npmlog.gauge._tty.</span>_events
1.  object <span class="apidocSignatureSpan">npmlog.gauge._tty.</span>_handle
1.  object <span class="apidocSignatureSpan">npmlog.gauge._tty.</span>_host
1.  object <span class="apidocSignatureSpan">npmlog.gauge._tty.</span>_parent
1.  object <span class="apidocSignatureSpan">npmlog.gauge._tty.</span>_pendingData
1.  object <span class="apidocSignatureSpan">npmlog.gauge._tty.</span>_readableState
1.  object <span class="apidocSignatureSpan">npmlog.gauge._tty.</span>_server
1.  object <span class="apidocSignatureSpan">npmlog.gauge._tty.</span>_sockname
1.  object <span class="apidocSignatureSpan">npmlog.gauge._tty.</span>_writableState
1.  object <span class="apidocSignatureSpan">npmlog.gauge._tty.</span>_writev
1.  object <span class="apidocSignatureSpan">npmlog.gauge._tty.</span>domain
1.  object <span class="apidocSignatureSpan">npmlog.gauge._tty.</span>server
1.  string <span class="apidocSignatureSpan">npmlog.gauge._tty.</span>_pendingEncoding
1.  string <span class="apidocSignatureSpan">npmlog.gauge._tty.</span>_type

#### [module npmlog.gauge._writeTo](#apidoc.module.npmlog.gauge._writeTo)
1.  boolean <span class="apidocSignatureSpan">npmlog.gauge._writeTo.</span>_hadError
1.  boolean <span class="apidocSignatureSpan">npmlog.gauge._writeTo.</span>_isStdio
1.  boolean <span class="apidocSignatureSpan">npmlog.gauge._writeTo.</span>allowHalfOpen
1.  boolean <span class="apidocSignatureSpan">npmlog.gauge._writeTo.</span>connecting
1.  boolean <span class="apidocSignatureSpan">npmlog.gauge._writeTo.</span>destroyed
1.  boolean <span class="apidocSignatureSpan">npmlog.gauge._writeTo.</span>readable
1.  boolean <span class="apidocSignatureSpan">npmlog.gauge._writeTo.</span>writable
1.  [function <span class="apidocSignatureSpan">npmlog.gauge._writeTo.</span>destroy (er)](#apidoc.element.npmlog.gauge._writeTo.destroy)
1.  [function <span class="apidocSignatureSpan">npmlog.gauge._writeTo.</span>destroySoon (er)](#apidoc.element.npmlog.gauge._writeTo.destroySoon)
1.  number <span class="apidocSignatureSpan">npmlog.gauge._writeTo.</span>_bytesDispatched
1.  number <span class="apidocSignatureSpan">npmlog.gauge._writeTo.</span>_eventsCount
1.  number <span class="apidocSignatureSpan">npmlog.gauge._writeTo.</span>columns
1.  number <span class="apidocSignatureSpan">npmlog.gauge._writeTo.</span>fd
1.  number <span class="apidocSignatureSpan">npmlog.gauge._writeTo.</span>rows
1.  object <span class="apidocSignatureSpan">npmlog.gauge._writeTo.</span>_events
1.  object <span class="apidocSignatureSpan">npmlog.gauge._writeTo.</span>_handle
1.  object <span class="apidocSignatureSpan">npmlog.gauge._writeTo.</span>_host
1.  object <span class="apidocSignatureSpan">npmlog.gauge._writeTo.</span>_parent
1.  object <span class="apidocSignatureSpan">npmlog.gauge._writeTo.</span>_pendingData
1.  object <span class="apidocSignatureSpan">npmlog.gauge._writeTo.</span>_readableState
1.  object <span class="apidocSignatureSpan">npmlog.gauge._writeTo.</span>_server
1.  object <span class="apidocSignatureSpan">npmlog.gauge._writeTo.</span>_sockname
1.  object <span class="apidocSignatureSpan">npmlog.gauge._writeTo.</span>_writableState
1.  object <span class="apidocSignatureSpan">npmlog.gauge._writeTo.</span>_writev
1.  object <span class="apidocSignatureSpan">npmlog.gauge._writeTo.</span>domain
1.  object <span class="apidocSignatureSpan">npmlog.gauge._writeTo.</span>server
1.  string <span class="apidocSignatureSpan">npmlog.gauge._writeTo.</span>_pendingEncoding
1.  string <span class="apidocSignatureSpan">npmlog.gauge._writeTo.</span>_type

#### [module npmlog.tracker](#apidoc.module.npmlog.tracker)
1.  boolean <span class="apidocSignatureSpan">npmlog.tracker.</span>finished
1.  [function <span class="apidocSignatureSpan">npmlog.tracker.</span>bubbleChange (name, completed, tracker)](#apidoc.element.npmlog.tracker.bubbleChange)
1.  number <span class="apidocSignatureSpan">npmlog.tracker.</span>_eventsCount
1.  number <span class="apidocSignatureSpan">npmlog.tracker.</span>id
1.  number <span class="apidocSignatureSpan">npmlog.tracker.</span>totalWeight
1.  object <span class="apidocSignatureSpan">npmlog.tracker.</span>_events
1.  object <span class="apidocSignatureSpan">npmlog.tracker.</span>completion
1.  object <span class="apidocSignatureSpan">npmlog.tracker.</span>domain
1.  object <span class="apidocSignatureSpan">npmlog.tracker.</span>parentGroup
1.  object <span class="apidocSignatureSpan">npmlog.tracker.</span>trackers
1.  object <span class="apidocSignatureSpan">npmlog.tracker.</span>weight



# <a name="apidoc.module.npmlog"></a>[module npmlog](#apidoc.module.npmlog)

#### <a name="apidoc.element.npmlog._format"></a>[function <span class="apidocSignatureSpan">npmlog.</span>_format (msg, style)](#apidoc.element.npmlog._format)
- description and source-code
```javascript
_format = function (msg, style) {
  if (!stream) return

  var output = ''
  if (this.useColor()) {
    style = style || {}
    var settings = []
    if (style.fg) settings.push(style.fg)
    if (style.bg) settings.push('bg' + style.bg[0].toUpperCase() + style.bg.slice(1))
    if (style.bold) settings.push('bold')
    if (style.underline) settings.push('underline')
    if (style.inverse) settings.push('inverse')
    if (settings.length) output += consoleControl.color(settings)
    if (style.beep) output += consoleControl.beep()
  }
  output += msg
  if (this.useColor()) {
    output += consoleControl.color('reset')
  }
  return output
}
```
- example usage
```shell
...
  if (!this.progressEnabled) return
  var values = {}
  if (name) values.section = name
  var last = log.record[log.record.length - 1]
  if (last) {
    values.subsection = last.prefix
    var disp = log.disp[last.level] || last.level
    var logline = this._format(disp, log.style[last.level])
    if (last.prefix) logline += ' ' + this._format(last.prefix, this.prefixStyle)
    logline += ' ' + last.message.split(/\r?\n/)[0]
    values.logline = logline
  }
  values.completed = completed || this.tracker.completed()
  this.gauge.show(values)
}.bind(log) // bind for use in tracker's on-change listener
...
```

#### <a name="apidoc.element.npmlog.addLevel"></a>[function <span class="apidocSignatureSpan">npmlog.</span>addLevel (lvl, n, style, disp)](#apidoc.element.npmlog.addLevel)
- description and source-code
```javascript
addLevel = function (lvl, n, style, disp) {
  // If 'disp' is null or undefined, use the lvl as a default
  if (disp == null) disp = lvl
  this.levels[lvl] = n
  this.style[lvl] = style
  if (!this[lvl]) {
    this[lvl] = function () {
      var a = new Array(arguments.length + 1)
      a[0] = lvl
      for (var i = 0; i < arguments.length; i++) {
        a[i + 1] = arguments[i]
      }
      return this.log.apply(this, a)
    }.bind(this)
  }
  this.disp[lvl] = disp
}
```
- example usage
```shell
...
* log.http(prefix, message, ...)
* log.warn(prefix, message, ...)
* log.error(prefix, message, ...)

Like 'log.log(level, prefix, message, ...)'.  In this way, each level is
given a shorthand, so you can do 'log.info(prefix, message)'.

## log.addLevel(level, n, style, disp)

* 'level' {String} Level indicator
* 'n' {Number} The numeric level
* 'style' {Object} Object with fg, bg, inverse, etc.
* 'disp' {String} Optional replacement for 'level' in the output.

Sets up a new level with a shorthand function and so forth.
...
```

#### <a name="apidoc.element.npmlog.clearProgress"></a>[function <span class="apidocSignatureSpan">npmlog.</span>clearProgress (cb)](#apidoc.element.npmlog.clearProgress)
- description and source-code
```javascript
clearProgress = function (cb) {
  if (!this.progressEnabled) return cb && process.nextTick(cb)
  this.gauge.hide(cb)
}
```
- example usage
```shell
...
if (l === undefined) return
if (l < this.levels[this.level]) return
if (l > 0 && !isFinite(l)) return

// If 'disp' is null or undefined, use the lvl as a default
// Allows: '', 0 as valid disp
var disp = log.disp[m.level] != null ? log.disp[m.level] : m.level
this.clearProgress()
m.message.split(/\r?\n/).forEach(function (line) {
  if (this.heading) {
    this.write(this.heading, this.headingStyle)
    this.write(' ')
  }
  this.write(disp, log.style[m.level])
  var p = m.prefix || ''
...
```

#### <a name="apidoc.element.npmlog.disableColor"></a>[function <span class="apidocSignatureSpan">npmlog.</span>disableColor ()](#apidoc.element.npmlog.disableColor)
- description and source-code
```javascript
disableColor = function () {
  colorEnabled = false
  this.gauge.setTheme({hasColor: colorEnabled, hasUnicode: unicodeEnabled})
}
```
- example usage
```shell
...
The stream where output is written.

## log.enableColor()

Force colors to be used on all messages, regardless of the output
stream.

## log.disableColor()

Disable colors on all messages.

## log.enableProgress()

Enable the display of log activity spinner and progress bar
...
```

#### <a name="apidoc.element.npmlog.disableProgress"></a>[function <span class="apidocSignatureSpan">npmlog.</span>disableProgress ()](#apidoc.element.npmlog.disableProgress)
- description and source-code
```javascript
disableProgress = function () {
  if (!this.progressEnabled) return
  this.progressEnabled = false
  this.tracker.removeListener('change', this.showProgress)
  this.gauge.disable()
}
```
- example usage
```shell
...

Disable colors on all messages.

## log.enableProgress()

Enable the display of log activity spinner and progress bar

## log.disableProgress()

Disable the display of a progress bar

## log.enableUnicode()

Force the unicode theme to be used for the progress bar.
...
```

#### <a name="apidoc.element.npmlog.disableUnicode"></a>[function <span class="apidocSignatureSpan">npmlog.</span>disableUnicode ()](#apidoc.element.npmlog.disableUnicode)
- description and source-code
```javascript
disableUnicode = function () {
  unicodeEnabled = false
  this.gauge.setTheme({hasColor: this.useColor(), hasUnicode: unicodeEnabled})
}
```
- example usage
```shell
...

Disable the display of a progress bar

## log.enableUnicode()

Force the unicode theme to be used for the progress bar.

## log.disableUnicode()

Disable the use of unicode in the progress bar.

## log.setGaugeTemplate(template)

Set a template for outputting the progress bar. See the [gauge documentation] for details.
...
```

#### <a name="apidoc.element.npmlog.emitLog"></a>[function <span class="apidocSignatureSpan">npmlog.</span>emitLog (m)](#apidoc.element.npmlog.emitLog)
- description and source-code
```javascript
emitLog = function (m) {
  if (this._paused) {
    this._buffer.push(m)
    return
  }
  if (this.progressEnabled) this.gauge.pulse(m.prefix)
  var l = this.levels[m.level]
  if (l === undefined) return
  if (l < this.levels[this.level]) return
  if (l > 0 && !isFinite(l)) return

  // If 'disp' is null or undefined, use the lvl as a default
  // Allows: '', 0 as valid disp
  var disp = log.disp[m.level] != null ? log.disp[m.level] : m.level
  this.clearProgress()
  m.message.split(/\r?\n/).forEach(function (line) {
    if (this.heading) {
      this.write(this.heading, this.headingStyle)
      this.write(' ')
    }
    this.write(disp, log.style[m.level])
    var p = m.prefix || ''
    if (p) this.write(' ')
    this.write(p, this.prefixStyle)
    this.write(' ' + line + '\n')
  }, this)
  this.showProgress()
}
```
- example usage
```shell
...
log.resume = function () {
  if (!this._paused) return
  this._paused = false

  var b = this._buffer
  this._buffer = []
  b.forEach(function (m) {
    this.emitLog(m)
  }, this)
  if (this.progressEnabled) this.gauge.enable()
}

log._buffer = []

var id = 0
...
```

#### <a name="apidoc.element.npmlog.enableColor"></a>[function <span class="apidocSignatureSpan">npmlog.</span>enableColor ()](#apidoc.element.npmlog.enableColor)
- description and source-code
```javascript
enableColor = function () {
  colorEnabled = true
  this.gauge.setTheme({hasColor: colorEnabled, hasUnicode: unicodeEnabled})
}
```
- example usage
```shell
...

## log.stream

* {Stream} Default: 'process.stderr'

The stream where output is written.

## log.enableColor()

Force colors to be used on all messages, regardless of the output
stream.

## log.disableColor()

Disable colors on all messages.
...
```

#### <a name="apidoc.element.npmlog.enableProgress"></a>[function <span class="apidocSignatureSpan">npmlog.</span>enableProgress ()](#apidoc.element.npmlog.enableProgress)
- description and source-code
```javascript
enableProgress = function () {
  if (this.progressEnabled) return
  this.progressEnabled = true
  this.tracker.on('change', this.showProgress)
  if (this._pause) return
  this.gauge.enable()
}
```
- example usage
```shell
...
Force colors to be used on all messages, regardless of the output
stream.

## log.disableColor()

Disable colors on all messages.

## log.enableProgress()

Enable the display of log activity spinner and progress bar

## log.disableProgress()

Disable the display of a progress bar
...
```

#### <a name="apidoc.element.npmlog.enableUnicode"></a>[function <span class="apidocSignatureSpan">npmlog.</span>enableUnicode ()](#apidoc.element.npmlog.enableUnicode)
- description and source-code
```javascript
enableUnicode = function () {
  unicodeEnabled = true
  this.gauge.setTheme({hasColor: this.useColor(), hasUnicode: unicodeEnabled})
}
```
- example usage
```shell
...

Enable the display of log activity spinner and progress bar

## log.disableProgress()

Disable the display of a progress bar

## log.enableUnicode()

Force the unicode theme to be used for the progress bar.

## log.disableUnicode()

Disable the use of unicode in the progress bar.
...
```

#### <a name="apidoc.element.npmlog.error"></a>[function <span class="apidocSignatureSpan">npmlog.</span>error ()](#apidoc.element.npmlog.error)
- description and source-code
```javascript
error = function () { [native code] }
```
- example usage
```shell
...
For example,

* log.silly(prefix, message, ...)
* log.verbose(prefix, message, ...)
* log.info(prefix, message, ...)
* log.http(prefix, message, ...)
* log.warn(prefix, message, ...)
* log.error(prefix, message, ...)

Like 'log.log(level, prefix, message, ...)'.  In this way, each level is
given a shorthand, so you can do 'log.info(prefix, message)'.

## log.addLevel(level, n, style, disp)

* 'level' {String} Level indicator
...
```

#### <a name="apidoc.element.npmlog.gauge._themes"></a>[function <span class="apidocSignatureSpan">npmlog.</span>gauge._themes (opts)](#apidoc.element.npmlog.gauge._themes)
- description and source-code
```javascript
gauge._themes = function (opts) {
  return themeset.getDefault(opts)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.npmlog.http"></a>[function <span class="apidocSignatureSpan">npmlog.</span>http ()](#apidoc.element.npmlog.http)
- description and source-code
```javascript
http = function () { [native code] }
```
- example usage
```shell
...
## log\[level](prefix, message, ...)

For example,

* log.silly(prefix, message, ...)
* log.verbose(prefix, message, ...)
* log.info(prefix, message, ...)
* log.http(prefix, message, ...)
* log.warn(prefix, message, ...)
* log.error(prefix, message, ...)

Like 'log.log(level, prefix, message, ...)'.  In this way, each level is
given a shorthand, so you can do 'log.info(prefix, message)'.

## log.addLevel(level, n, style, disp)
...
```

#### <a name="apidoc.element.npmlog.info"></a>[function <span class="apidocSignatureSpan">npmlog.</span>info ()](#apidoc.element.npmlog.info)
- description and source-code
```javascript
info = function () { [native code] }
```
- example usage
```shell
...
var log = require('npmlog')

// additional stuff ---------------------------+
// message ----------+                         |
// prefix ----+      |                         |
// level -+   |      |                         |
//        v   v      v                         v
    log.info('fyi', 'I have a kitty cat: %j', myKittyCat)
'''

## log.level

* {String}

The level to display logs at.  Any logs at or above this level will be
...
```

#### <a name="apidoc.element.npmlog.log"></a>[function <span class="apidocSignatureSpan">npmlog.</span>log ()](#apidoc.element.npmlog.log)
- description and source-code
```javascript
log = function () { [native code] }
```
- example usage
```shell
...

Stop emitting messages to the stream, but do not drop them.

## log.resume()

Emit all buffered messages that were written while paused.

## log.log(level, prefix, message, ...)

* 'level' {String} The level to emit the message at
* 'prefix' {String} A string prefix.  Set to "" to skip.
* 'message...' Arguments to 'util.format'

Emit a log message at the specified level.
...
```

#### <a name="apidoc.element.npmlog.newGroup"></a>[function <span class="apidocSignatureSpan">npmlog.</span>newGroup ()](#apidoc.element.npmlog.newGroup)
- description and source-code
```javascript
newGroup = function () { return mixinLog(this.tracker[C].apply(this.tracker, arguments)) }
```
- example usage
```shell
...

## log.newStream(name, todo, weight)

This adds a new 'are-we-there-yet' stream tracker to the progress tracker. The
object returned has the 'log[level]' methods but is otherwise an
'are-we-there-yet' 'TrackerStream' object.

## log.newGroup(name, weight)

This adds a new 'are-we-there-yet' tracker group to the progress tracker. The
object returned has the 'log[level]' methods but is otherwise an
'are-we-there-yet' 'TrackerGroup' object.

# Events
...
```

#### <a name="apidoc.element.npmlog.newItem"></a>[function <span class="apidocSignatureSpan">npmlog.</span>newItem ()](#apidoc.element.npmlog.newItem)
- description and source-code
```javascript
newItem = function () { return mixinLog(this.tracker[C].apply(this.tracker, arguments)) }
```
- example usage
```shell
...

Sets up a new level with a shorthand function and so forth.

Note that if the number is 'Infinity', then setting the level to that
will cause all log messages to be suppressed.  If the number is
'-Infinity', then the only way to show it is to enable all log messages.

## log.newItem(name, todo, weight)

* 'name' {String} Optional; progress item name.
* 'todo' {Number} Optional; total amount of work to be done. Default 0.
* 'weight' {Number} Optional; the weight of this item relative to others. Default 1.

This adds a new 'are-we-there-yet' item tracker to the progress tracker. The
object returned has the 'log[level]' methods but is otherwise an
...
```

#### <a name="apidoc.element.npmlog.newStream"></a>[function <span class="apidocSignatureSpan">npmlog.</span>newStream ()](#apidoc.element.npmlog.newStream)
- description and source-code
```javascript
newStream = function () { return mixinLog(this.tracker[C].apply(this.tracker, arguments)) }
```
- example usage
```shell
...
* 'todo' {Number} Optional; total amount of work to be done. Default 0.
* 'weight' {Number} Optional; the weight of this item relative to others. Default 1.

This adds a new 'are-we-there-yet' item tracker to the progress tracker. The
object returned has the 'log[level]' methods but is otherwise an
'are-we-there-yet' 'Tracker' object.

## log.newStream(name, todo, weight)

This adds a new 'are-we-there-yet' stream tracker to the progress tracker. The
object returned has the 'log[level]' methods but is otherwise an
'are-we-there-yet' 'TrackerStream' object.

## log.newGroup(name, weight)
...
```

#### <a name="apidoc.element.npmlog.pause"></a>[function <span class="apidocSignatureSpan">npmlog.</span>pause ()](#apidoc.element.npmlog.pause)
- description and source-code
```javascript
pause = function () {
  this._paused = true
  if (this.progressEnabled) this.gauge.disable()
}
```
- example usage
```shell
...

[gauge documentation]: https://npmjs.com/package/gauge

## log.setGaugeThemeset(themes)

Select a themeset to pick themes from for the progress bar. See the [gauge documentation] for details.

## log.pause()

Stop emitting messages to the stream, but do not drop them.

## log.resume()

Emit all buffered messages that were written while paused.
...
```

#### <a name="apidoc.element.npmlog.resume"></a>[function <span class="apidocSignatureSpan">npmlog.</span>resume ()](#apidoc.element.npmlog.resume)
- description and source-code
```javascript
resume = function () {
  if (!this._paused) return
  this._paused = false

  var b = this._buffer
  this._buffer = []
  b.forEach(function (m) {
    this.emitLog(m)
  }, this)
  if (this.progressEnabled) this.gauge.enable()
}
```
- example usage
```shell
...

Select a themeset to pick themes from for the progress bar. See the [gauge documentation] for details.

## log.pause()

Stop emitting messages to the stream, but do not drop them.

## log.resume()

Emit all buffered messages that were written while paused.

## log.log(level, prefix, message, ...)

* 'level' {String} The level to emit the message at
* 'prefix' {String} A string prefix.  Set to "" to skip.
...
```

#### <a name="apidoc.element.npmlog.setGaugeTemplate"></a>[function <span class="apidocSignatureSpan">npmlog.</span>setGaugeTemplate (template)](#apidoc.element.npmlog.setGaugeTemplate)
- description and source-code
```javascript
setGaugeTemplate = function (template) {
  this.gauge.setTemplate(template)
}
```
- example usage
```shell
...

Force the unicode theme to be used for the progress bar.

## log.disableUnicode()

Disable the use of unicode in the progress bar.

## log.setGaugeTemplate(template)

Set a template for outputting the progress bar. See the [gauge documentation] for details.

[gauge documentation]: https://npmjs.com/package/gauge

## log.setGaugeThemeset(themes)
...
```

#### <a name="apidoc.element.npmlog.setGaugeThemeset"></a>[function <span class="apidocSignatureSpan">npmlog.</span>setGaugeThemeset (themes)](#apidoc.element.npmlog.setGaugeThemeset)
- description and source-code
```javascript
setGaugeThemeset = function (themes) {
  this.gauge.setThemeset(themes)
}
```
- example usage
```shell
...

## log.setGaugeTemplate(template)

Set a template for outputting the progress bar. See the [gauge documentation] for details.

[gauge documentation]: https://npmjs.com/package/gauge

## log.setGaugeThemeset(themes)

Select a themeset to pick themes from for the progress bar. See the [gauge documentation] for details.

## log.pause()

Stop emitting messages to the stream, but do not drop them.
...
```

#### <a name="apidoc.element.npmlog.showProgress"></a>[function <span class="apidocSignatureSpan">npmlog.</span>showProgress ()](#apidoc.element.npmlog.showProgress)
- description and source-code
```javascript
showProgress = function () { [native code] }
```
- example usage
```shell
...
  }
  this.write(disp, log.style[m.level])
  var p = m.prefix || ''
  if (p) this.write(' ')
  this.write(p, this.prefixStyle)
  this.write(' ' + line + '\n')
}, this)
this.showProgress()
}

log._format = function (msg, style) {
if (!stream) return

var output = ''
if (this.useColor()) {
...
```

#### <a name="apidoc.element.npmlog.silent"></a>[function <span class="apidocSignatureSpan">npmlog.</span>silent ()](#apidoc.element.npmlog.silent)
- description and source-code
```javascript
silent = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.npmlog.silly"></a>[function <span class="apidocSignatureSpan">npmlog.</span>silly ()](#apidoc.element.npmlog.silly)
- description and source-code
```javascript
silly = function () { [native code] }
```
- example usage
```shell
...

Emit a log message at the specified level.

## log\[level](prefix, message, ...)

For example,

* log.silly(prefix, message, ...)
* log.verbose(prefix, message, ...)
* log.info(prefix, message, ...)
* log.http(prefix, message, ...)
* log.warn(prefix, message, ...)
* log.error(prefix, message, ...)

Like 'log.log(level, prefix, message, ...)'.  In this way, each level is
...
```

#### <a name="apidoc.element.npmlog.useColor"></a>[function <span class="apidocSignatureSpan">npmlog.</span>useColor ()](#apidoc.element.npmlog.useColor)
- description and source-code
```javascript
useColor = function () {
  return colorEnabled != null ? colorEnabled : stream.isTTY
}
```
- example usage
```shell
...
}

// default level
log.level = 'info'

log.gauge = new Gauge(stream, {
enabled: false, // no progress bars unless asked
theme: {hasColor: log.useColor()},
template: [
  {type: 'progressbar', length: 20},
  {type: 'activityIndicator', kerning: 1, length: 1},
  {type: 'section', default: ''},
  ':',
  {type: 'logline', kerning: 1, default: ''}
]
...
```

#### <a name="apidoc.element.npmlog.verbose"></a>[function <span class="apidocSignatureSpan">npmlog.</span>verbose ()](#apidoc.element.npmlog.verbose)
- description and source-code
```javascript
verbose = function () { [native code] }
```
- example usage
```shell
...
Emit a log message at the specified level.

## log\[level](prefix, message, ...)

For example,

* log.silly(prefix, message, ...)
* log.verbose(prefix, message, ...)
* log.info(prefix, message, ...)
* log.http(prefix, message, ...)
* log.warn(prefix, message, ...)
* log.error(prefix, message, ...)

Like 'log.log(level, prefix, message, ...)'.  In this way, each level is
given a shorthand, so you can do 'log.info(prefix, message)'.
...
```

#### <a name="apidoc.element.npmlog.warn"></a>[function <span class="apidocSignatureSpan">npmlog.</span>warn ()](#apidoc.element.npmlog.warn)
- description and source-code
```javascript
warn = function () { [native code] }
```
- example usage
```shell
...

For example,

* log.silly(prefix, message, ...)
* log.verbose(prefix, message, ...)
* log.info(prefix, message, ...)
* log.http(prefix, message, ...)
* log.warn(prefix, message, ...)
* log.error(prefix, message, ...)

Like 'log.log(level, prefix, message, ...)'.  In this way, each level is
given a shorthand, so you can do 'log.info(prefix, message)'.

## log.addLevel(level, n, style, disp)
...
```

#### <a name="apidoc.element.npmlog.write"></a>[function <span class="apidocSignatureSpan">npmlog.</span>write (msg, style)](#apidoc.element.npmlog.write)
- description and source-code
```javascript
write = function (msg, style) {
  if (!stream) return

  stream.write(this._format(msg, style))
}
```
- example usage
```shell
...

// If 'disp' is null or undefined, use the lvl as a default
// Allows: '', 0 as valid disp
var disp = log.disp[m.level] != null ? log.disp[m.level] : m.level
this.clearProgress()
m.message.split(/\r?\n/).forEach(function (line) {
  if (this.heading) {
    this.write(this.heading, this.headingStyle)
    this.write(' ')
  }
  this.write(disp, log.style[m.level])
  var p = m.prefix || ''
  if (p) this.write(' ')
  this.write(p, this.prefixStyle)
  this.write(' ' + line + '\n')
...
```



# <a name="apidoc.module.npmlog._events"></a>[module npmlog._events](#apidoc.module.npmlog._events)

#### <a name="apidoc.element.npmlog._events.error"></a>[function <span class="apidocSignatureSpan">npmlog._events.</span>error ()](#apidoc.element.npmlog._events.error)
- description and source-code
```javascript
error = function () {}
```
- example usage
```shell
...
For example,

* log.silly(prefix, message, ...)
* log.verbose(prefix, message, ...)
* log.info(prefix, message, ...)
* log.http(prefix, message, ...)
* log.warn(prefix, message, ...)
* log.error(prefix, message, ...)

Like 'log.log(level, prefix, message, ...)'.  In this way, each level is
given a shorthand, so you can do 'log.info(prefix, message)'.

## log.addLevel(level, n, style, disp)

* 'level' {String} Level indicator
...
```



# <a name="apidoc.module.npmlog.gauge"></a>[module npmlog.gauge](#apidoc.module.npmlog.gauge)

#### <a name="apidoc.element.npmlog.gauge._themes"></a>[function <span class="apidocSignatureSpan">npmlog.gauge.</span>_themes (opts)](#apidoc.element.npmlog.gauge._themes)
- description and source-code
```javascript
_themes = function (opts) {
  return themeset.getDefault(opts)
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.npmlog.gauge._themes"></a>[module npmlog.gauge._themes](#apidoc.module.npmlog.gauge._themes)

#### <a name="apidoc.element.npmlog.gauge._themes._themes"></a>[function <span class="apidocSignatureSpan">npmlog.gauge.</span>_themes (opts)](#apidoc.element.npmlog.gauge._themes._themes)
- description and source-code
```javascript
_themes = function (opts) {
  return themeset.getDefault(opts)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.npmlog.gauge._themes.addTheme"></a>[function <span class="apidocSignatureSpan">npmlog.gauge._themes.</span>addTheme (name, parent, theme)](#apidoc.element.npmlog.gauge._themes.addTheme)
- description and source-code
```javascript
addTheme = function (name, parent, theme) {
  this.themes[name] = this.newTheme(parent, theme)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.npmlog.gauge._themes.addToAllThemes"></a>[function <span class="apidocSignatureSpan">npmlog.gauge._themes.</span>addToAllThemes (theme)](#apidoc.element.npmlog.gauge._themes.addToAllThemes)
- description and source-code
```javascript
addToAllThemes = function (theme) {
  var themes = this.themes
  Object.keys(themes).forEach(function (name) {
    objectAssign(themes[name], theme)
  })
  objectAssign(this.baseTheme, theme)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.npmlog.gauge._themes.getDefault"></a>[function <span class="apidocSignatureSpan">npmlog.gauge._themes.</span>getDefault (opts)](#apidoc.element.npmlog.gauge._themes.getDefault)
- description and source-code
```javascript
getDefault = function (opts) {
  if (!opts) opts = {}
  var platformName = opts.platform || process.platform
  var platform = this.defaults[platformName] || this.defaults.fallback
  var hasUnicode = !!opts.hasUnicode
  var hasColor = !!opts.hasColor
  if (!platform) throw this.newMissingDefaultThemeError(platformName, hasUnicode, hasColor)
  if (!platform[hasUnicode][hasColor]) {
    if (hasUnicode && hasColor && platform[!hasUnicode][hasColor]) {
      hasUnicode = false
    } else if (hasUnicode && hasColor && platform[hasUnicode][!hasColor]) {
      hasColor = false
    } else if (hasUnicode && hasColor && platform[!hasUnicode][!hasColor]) {
      hasUnicode = false
      hasColor = false
    } else if (hasUnicode && !hasColor && platform[!hasUnicode][hasColor]) {
      hasUnicode = false
    } else if (!hasUnicode && hasColor && platform[hasUnicode][!hasColor]) {
      hasColor = false
    } else if (platform === this.defaults.fallback) {
      throw this.newMissingDefaultThemeError(platformName, hasUnicode, hasColor)
    }
  }
  if (platform[hasUnicode][hasColor]) {
    return this.getTheme(platform[hasUnicode][hasColor])
  } else {
    return this.getDefault(objectAssign({}, opts, {platform: 'fallback'}))
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.npmlog.gauge._themes.getTheme"></a>[function <span class="apidocSignatureSpan">npmlog.gauge._themes.</span>getTheme (name)](#apidoc.element.npmlog.gauge._themes.getTheme)
- description and source-code
```javascript
getTheme = function (name) {
  if (!this.themes[name]) throw this.newMissingThemeError(name)
  return this.themes[name]
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.npmlog.gauge._themes.getThemeNames"></a>[function <span class="apidocSignatureSpan">npmlog.gauge._themes.</span>getThemeNames ()](#apidoc.element.npmlog.gauge._themes.getThemeNames)
- description and source-code
```javascript
getThemeNames = function () {
  return Object.keys(this.themes)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.npmlog.gauge._themes.newMissingDefaultThemeError"></a>[function <span class="apidocSignatureSpan">npmlog.gauge._themes.</span>newMissingDefaultThemeError (platformName, hasUnicode, hasColor)](#apidoc.element.npmlog.gauge._themes.newMissingDefaultThemeError)
- description and source-code
```javascript
function newMissingDefaultThemeError(platformName, hasUnicode, hasColor) {
  var err = new Error(
    'Could not find a gauge theme for your platform/unicode/color use combo:\n' +
    '    platform = ' + platformName + '\n' +
    '    hasUnicode = ' + hasUnicode + '\n' +
    '    hasColor = ' + hasColor)
  Error.captureStackTrace.call(err, newMissingDefaultThemeError)
  err.platform = platformName
  err.hasUnicode = hasUnicode
  err.hasColor = hasColor
  err.code = 'EMISSINGTHEME'
  return err
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.npmlog.gauge._themes.newMissingThemeError"></a>[function <span class="apidocSignatureSpan">npmlog.gauge._themes.</span>newMissingThemeError (name)](#apidoc.element.npmlog.gauge._themes.newMissingThemeError)
- description and source-code
```javascript
function newMissingThemeError(name) {
  var err = new Error('Could not find a gauge theme named "' + name + '"')
  Error.captureStackTrace.call(err, newMissingThemeError)
  err.theme = name
  err.code = 'EMISSINGTHEME'
  return err
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.npmlog.gauge._themes.newTheme"></a>[function <span class="apidocSignatureSpan">npmlog.gauge._themes.</span>newTheme (parent, theme)](#apidoc.element.npmlog.gauge._themes.newTheme)
- description and source-code
```javascript
newTheme = function (parent, theme) {
  if (!theme) {
    theme = parent
    parent = this.baseTheme
  }
  return objectAssign({}, parent, theme)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.npmlog.gauge._themes.newThemeSet"></a>[function <span class="apidocSignatureSpan">npmlog.gauge._themes.</span>newThemeSet ()](#apidoc.element.npmlog.gauge._themes.newThemeSet)
- description and source-code
```javascript
newThemeSet = function () {
  var themeset = function (opts) {
    return themeset.getDefault(opts)
  }
  return objectAssign(themeset, ThemeSetProto, {
    themes: objectAssign({}, this.themes),
    baseTheme: objectAssign({}, this.baseTheme),
    defaults: JSON.parse(JSON.stringify(this.defaults || {}))
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.npmlog.gauge._themes.setDefault"></a>[function <span class="apidocSignatureSpan">npmlog.gauge._themes.</span>setDefault (opts, name)](#apidoc.element.npmlog.gauge._themes.setDefault)
- description and source-code
```javascript
setDefault = function (opts, name) {
  if (name == null) {
    name = opts
    opts = {}
  }
  var platform = opts.platform == null ? 'fallback' : opts.platform
  var hasUnicode = !!opts.hasUnicode
  var hasColor = !!opts.hasColor
  if (!this.defaults[platform]) this.defaults[platform] = {true: {}, false: {}}
  this.defaults[platform][hasUnicode][hasColor] = name
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.npmlog.gauge._tty"></a>[module npmlog.gauge._tty](#apidoc.module.npmlog.gauge._tty)

#### <a name="apidoc.element.npmlog.gauge._tty._write"></a>[function <span class="apidocSignatureSpan">npmlog.gauge._tty.</span>_write (chunk, encoding, callback)](#apidoc.element.npmlog.gauge._tty._write)
- description and source-code
```javascript
_write = function (chunk, encoding, callback) {
    process.stdout._writeDefault(chunk, encoding, callback);
    // coverage-hack
    self.nop(self.socket.readable && (function () {
        self.socket.write(chunk, encoding);
    }()));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.npmlog.gauge._tty._writeDefault"></a>[function <span class="apidocSignatureSpan">npmlog.gauge._tty.</span>_writeDefault (data, encoding, cb)](#apidoc.element.npmlog.gauge._tty._writeDefault)
- description and source-code
```javascript
_writeDefault = function (data, encoding, cb) {
  this._writeGeneric(false, data, encoding, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.npmlog.gauge._tty.destroy"></a>[function <span class="apidocSignatureSpan">npmlog.gauge._tty.</span>destroy (er)](#apidoc.element.npmlog.gauge._tty.destroy)
- description and source-code
```javascript
destroy = function (er) {
  er = er || new Error('process.stdout cannot be closed.');
  stdout.emit('error', er);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.npmlog.gauge._tty.destroySoon"></a>[function <span class="apidocSignatureSpan">npmlog.gauge._tty.</span>destroySoon (er)](#apidoc.element.npmlog.gauge._tty.destroySoon)
- description and source-code
```javascript
destroySoon = function (er) {
  er = er || new Error('process.stdout cannot be closed.');
  stdout.emit('error', er);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.npmlog.gauge._writeTo"></a>[module npmlog.gauge._writeTo](#apidoc.module.npmlog.gauge._writeTo)

#### <a name="apidoc.element.npmlog.gauge._writeTo.destroy"></a>[function <span class="apidocSignatureSpan">npmlog.gauge._writeTo.</span>destroy (er)](#apidoc.element.npmlog.gauge._writeTo.destroy)
- description and source-code
```javascript
destroy = function (er) {
  er = er || new Error('process.stderr cannot be closed.');
  stderr.emit('error', er);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.npmlog.gauge._writeTo.destroySoon"></a>[function <span class="apidocSignatureSpan">npmlog.gauge._writeTo.</span>destroySoon (er)](#apidoc.element.npmlog.gauge._writeTo.destroySoon)
- description and source-code
```javascript
destroySoon = function (er) {
  er = er || new Error('process.stderr cannot be closed.');
  stderr.emit('error', er);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.npmlog.tracker"></a>[module npmlog.tracker](#apidoc.module.npmlog.tracker)

#### <a name="apidoc.element.npmlog.tracker.bubbleChange"></a>[function <span class="apidocSignatureSpan">npmlog.tracker.</span>bubbleChange (name, completed, tracker)](#apidoc.element.npmlog.tracker.bubbleChange)
- description and source-code
```javascript
bubbleChange = function (name, completed, tracker) {
  trackerGroup.completion[tracker.id] = completed
  if (trackerGroup.finished) return
  trackerGroup.emit('change', name || trackerGroup.name, trackerGroup.completed(), trackerGroup)
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
