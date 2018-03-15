How to use

1. Add using KSBankMellat; to top of the class.

2. Create new instance :
	var pgc = new PaymentGatewayClient();

3. Use methods as documention :
	
	var result = await pgc.bpPayRequestAsync(terminalId, userName, password, orderId, amout, localDate, localTime, additionalData, callBackUrl, payerId);
	string[] resultArray = result.Body.@return.Split(",");
	if(resultArray[0] == "0")
    {
        //Send user to gateway
    }
    else
    {
        //Show error message
    }