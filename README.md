# AggressorScripts

Simple Aggressor Scripts for CobaltStrike.

## SeatbeltOutput.cna
It will detect whenever Seatbelt output is in the console of CS, parse the output and save it to an attacker defined local log folder.

## SharpDPAPIOutput.cna
It will detect whenever SharpDPAPI output is in the console of CS, parse the output and save it to an attacker defined local log folder.

**Note**
SharpDPAPI has been modified to output the following string upon completion in order for the script to be able to search for it:

```patch
@@ -26,6 +26,7 @@ namespace SharpDPAPI
                     // show the usage if no commands were found for the command name
                     if (commandFound == false)
                         Info.ShowUsage();
+                    Console.WriteLine("\r\n[*] Finished SharpDPAPI execution");
                 }
             }
             catch (Exception e)
```
