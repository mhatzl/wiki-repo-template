{{
  
This section contains requirements for the system.

The folder structure reflects the intended workflow on how requirements should be handled.

1. Requirements are **proposed**, and moved into the `5.v-REQprop` folder
2. Once a requirement has enough information available to be implemented, it is **ready**, and should be moved to the `5.w-REQrdy` folder
3. A requirement in **proposed** or **ready** state may be **declined**, meaning that it will not be implemented, and must be moved to the `5.z-REQdecl` folder
4. When the implementation of a requirement is merged into the *main* branch, the requirement gets **active**, and must be moved to the `5.a-REQact` folder
5. If a requirement is replaced or removed by another requirement or decision record, the requirement gets **deprecated**, and must be moved to the `5.y-REQdepr` folder 

   **Note:** A link must be added to the **deprecated** requirement, pointing to the new requirement or decision record.

}}
