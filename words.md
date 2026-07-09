- workspace => Overall apps
few improtant command :
1. npm init -y
2. pnpm add -Dw lerna
3. npx lerna init

create react app in apps folder :
1. pnpm create vite apps/customer-portal --template react-ts  

# to run only cusotmer-portal app so run this command:
1. pnpm --filter customer-portal dev

# we create the custom internal package where we create the reusable UI code like button so we can use this as a internal package in the apps/ multiple UI appkication like cusotmer0support, admin, maiwebui etc.

## so befire using the in apps/ deffirent ui app first we have to install it.
## packages folder we create ui packehe so install from root folder : fe-lifecycle :
1. FE-LIFECYCLE> pnpm add @repo/ui@workspace:* --filter customer-portal 


# how to use typescript-config as a file 
> pnpm add @repo/eslint-config@workspace:* --filter customer-portal


# how to use utils as a package
> pnpm add @repo/utils@workspace:* --filter customer-portal

## to run this application : 
> pnpm dev


## Unit test setup :
run this command on root level: 
> pnpm add -Dw jest jest-environment-jsdom ts-jest @types/jest @testing-library/react @testing-library/jest-dom @testing-library/user-event

# use jest testing config as package in the customer -portal app
> pnpm add @repo/jest-config@workspace:* --filter customer-portal


# after jest testing we setup the sonarqube cloud 
where we create account by github abd then select repositiory and the  we see the summary of the repo code and it generate the report .
after that we go inot the adminitration to disable the automatic analysis of the repo code
1. we do setup like when we puch code to github repo so that time only he test and analyze the repo code and generate the report.

2. for that we go inot the proejct inforation collect proejct key and organization key and also create the token by click on the user account and set up this token into the github repo secret and variable with n ame SONAR_TOKEN

3. then go into the vs-code and do the furthur steps
