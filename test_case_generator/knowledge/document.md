### My docs
add user to Workday process
Add Employee to Workday 

# Conversion Test Cases: IHA DB Service Partner to Workday SP

## Convert IHA DB SP to WD SP with IHA LocationID (SJSEMI1258)  

### Preconditions:
- IHA DB Service Partner Identity in IDNow
- Check that user is not in Workday already
- Validate user attributes in IDNow
  - CorpAD Account
  - IHA AD Account

### Test Steps:
- Workday create new Service Partner from IHA user info
  - Provide Workday people current 4x4 
  - locationlD = SJSEMI1258 (Ann Arbor IHA)
- Do full Workday aggregation
- Verify Identity

### Expected Results:
- New Workday account created for Identity
- Validate identity is updated with all Workday info
- Validate downstream systems are updated with Workday info
- Ensure no accounts were deleted 


## Convert IHA DB SP to WD SP without IHA locationlD (use any other 1700 location ID's other than SJSEMI1258)

### Preconditions:
- IHA DB Service Partner Identity in IDNow
- Check that user is not in Workday already
- Validate user attributes in IDNow
  - CorpAD Account
  - IHA AD Account

### Test Steps:
- Workday create new Service Partner from IHA user info
  - Provide Workday people current 4x4 
  - locationlD = anything other than SJSEMI1258 (Ann Arbor IHA)
- Do full Workday aggregation
- Verify Identity

### Expected Results:
- New Workday account created for Identity
- Validate identity is updated with all Workday info
- Validate downstream systems are updated with Workday info
- Ensure only IHA AD account is deleted

# Conversion Test Cases: IHA DB Service Partner to Workday Employee

## Convert IHA DB SP to WD Employee with IHA locationlD (SJSEMI1258)

### Preconditions:
- IHA DB Service Partner Identity in IDNow
- Validate user attributes

### Test Steps:
- Workday create new Employee from IHA user info
  - locationlD = SJSEMI1258 (Ann Arbor IHA)
- Aggregate Workday account
- Verify new Identity
- Reconcile Identities
  - Old 4x4 retained and new attributes merged to old identity
  - Follow IHA account reconciliation doc

### Expected Results:
- New Employee created with new 4x4
- New 4x4 written back to Workday
- New IHA AD account
- New Corp AD account
- Still working on this test case

## Convert IHA DB SP & WD SP to WD SP with location ID (SJSEMI1258) of IHA


## Convert IHA DB SP to WD Employee without IHA locationlD (use any other 1700 location ID's other than SJSEMI1258)

## Convert IHA DB SP to WD SP without IHA locationlD (use any other 1700 location ID's other than SJSEMI1258)
