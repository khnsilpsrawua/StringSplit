# StringSplit
Func _StringRegExpSplit($sString, $sPattern)     Local $aRet[2] = [1, $sString], $sSplit = StringRegExpReplace($sString, $sPattern, '___SPLIT___')     If @error Then Return SetError(2, @extended, $aRet)     If 0 = @extended Then Return SetError(1, 0, $aRet)     Return StringSplit($sSplit, '___SPLIT___', 1) EndFunc ;==>_StringRegExpSplit
