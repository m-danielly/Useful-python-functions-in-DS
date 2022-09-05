    last_n_day
    
    
    ```python
    def last_n_day(n= 1, frmt='%Y%m%d', string=False):
        '''
        

        Parameters
        ----------
        n : TYPE, optional
            last -n th day from today. The default is 1 which return Yesterday.
        frmt : TYPE, optional
            output date format. The default is '%Y%m%d'.
        string : TYPE, optional
            return string format output if True.

        Returns
        -------
        TYPE
            DESCRIPTION.

        '''
        from datetime import date, timedelta
        temp_day = date.today() - datetime.timedelta(days = n)
        if string:
            return temp_day.strftime(frmt)
        else:
            return temp_day
    
    transfer_file = f'{transFile}{last_n_day():%Y%m%d}.csv'
    
    transFile='DC_cashback_Recharge_'
    transfer_file = f'{transFile}_{last_n_day():%Y%m%d}.csv'
    
    
    ```
