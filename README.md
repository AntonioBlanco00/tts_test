# tts_test
Componente para probar el TTS en EBO.
Envía string al componente "melotts_robolab" para que dicho commponente reproduzca por altavoz el TTS.


## Configuration parameters
As any other component, *tts_test* needs a configuration file to start. In
```
etc/config
```
you can find an example of a configuration file. We can find there the following lines:
```
# Endpoints for implements interfaces
# Proxies for required interfaces
SpeechProxy = speech:tcp -h localhost -p 11339


Ice.Warn.Connections=0
Ice.Trace.Network=0
Ice.Trace.Protocol=0
Ice.MessageSizeMax=20004800

```

## Starting the component
To avoid changing the *config* file in the repository, we can copy it to the component's home directory, so changes will remain untouched by future git pulls:

```
cd <tts_test's path> 
```
```
cp etc/config config
```

After editing the new config file we can run the component:

```
src/tts_test.py etc/config
```
