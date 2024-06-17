# Creating a Virtual Private Cloud using Terraform {#rosa-hcp-vpc-terraform .task}

Terraform is a tool that allows you to create various resources using an established template. The following process uses the default options as required to create a ROSA with HCP cluster. For more information about using Terraform, see the additional resources.

Prerequisites

-   You have installed Terraform version 1.4.0 or newer on your machine.
-   You have installed Git on your machine.

1.  Open a shell prompt and clone the Terraform VPC repository by running the following command:

    ```
    $ git clone https://github.com/openshift-cs/terraform-vpc-example
    ```

2.  Navigate to the created directory by running the following command:

    ```
    $ cd terraform-vpc-example
    ```

3.  Initiate the Terraform file by running the following command:

    ```
    $ terraform init
    ```

    A message confirming the initialization appears when this process completes.

4.  To build your VPC Terraform plan based on the existing Terraform template, run the plan command. You must include your AWS region. You can choose to specify a cluster name. A rosa.tfplan file is added to the hypershift-tf directory after the terraform plan completes. For more detailed options, see the Terraform VPC repository’s README file.

    ```
    $ terraform plan -out rosa.tfplan -var region=<region>
    ```

5.  Apply this plan file to build your VPC by running the following command:

    ```
    $ terraform apply rosa.tfplan
    ```

    1.  You can capture the values of the Terraform-provisioned private, public, and machinepool subnet IDs as environment variables to use when creating your ROSA with HCP cluster by running the following commands:

        ```
        $ export SUBNET_IDS=$(terraform output -raw cluster-subnets-string)
        ```

    2.  Verify that the variables were correctly set with the following command:

        ```
        $ echo $SUBNET_IDS
        ```

        ```
        $ subnet-0a6a57e0f784171aa,subnet-078e84e5b10ecf5b0
        ```


Additional resources

-   See the Terraform VPC repository for a detailed list of all options available when customizing the VPC for your needs.

