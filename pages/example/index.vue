<template>
  <div class="wrapper example">
    <section class="typography">
      <h1 class="m-t-0">Typography</h1>

      <ul>
        <li class="h1">H1</li>
        <li class="h2">H2</li>
        <li class="h3">H3</li>
        <li class="h4">H4</li>
        <li class="h5">H5</li>
        <li class="text-1-b">Body text 1 bold</li>
        <li class="text-1-m">Body text 1 med</li>
        <li class="text-2-m">Body text 2 med</li>
        <li class="text-2">Body text 2 reg</li>
        <li class="text-3">Body text 3 reg</li>
        <li class="text-3-m">Body text 3 med</li>
        <li class="text-4">Body text 4</li>
      </ul>
    </section>

    <section class="colors">
      <h1>Colors</h1>

      <div class="inline-block m-r-a m-l-a">
        <div class="flex flex-wrap__wrap gap-24 m-b-16">
          <div class="color-box">
            <div class="preview" style="background-color: var(--primary)"></div>
            <div class="name">primary</div>
            <div class="property">358F94</div>
          </div>

          <div class="color-box">
            <div
              class="preview"
              style="background-color: var(--secondary)"
            ></div>
            <div class="name">secondary</div>
            <div class="property">f59a28</div>
          </div>

          <div class="color-box">
            <div
              class="preview"
              style="background-color: var(--primary-light)"
            ></div>
            <div class="name">primary-light</div>
            <div class="property">e6eff0</div>
          </div>

          <div class="color-box">
            <div class="preview" style="background-color: var(--error)"></div>
            <div class="name">error</div>
            <div class="property">d55d5d</div>
          </div>

          <div class="color-box">
            <div
              class="preview"
              style="background-color: var(--color-success)"
            ></div>
            <div class="name">color-success</div>
            <div class="property">359440</div>
          </div>
        </div>

        <div class="flex flex-wrap__wrap gap-24">
          <div class="color-box">
            <div class="preview" style="background-color: var(--bg-form)"></div>
            <div class="name">bg-form</div>
            <div class="property">358F94, 10%</div>
          </div>

          <div class="color-box">
            <div class="preview" style="background-color: var(--bg-main)"></div>
            <div class="name">bg-main</div>
            <div class="property">fafafa</div>
          </div>

          <div class="color-box">
            <div class="preview" style="background-color: var(--light)"></div>
            <div class="name">light</div>
            <div class="property">ffffff</div>
          </div>

          <div class="color-box">
            <div class="preview" style="background-color: var(--dark)"></div>
            <div class="name">dark</div>
            <div class="property">000000</div>
          </div>

          <div class="color-box">
            <div
              class="preview"
              style="background-color: var(--color-minor)"
            ></div>
            <div class="name">color-minor</div>
            <div class="property">4d5974</div>
          </div>
        </div>
      </div>
    </section>

    <section class="buttons">
      <h1>Buttons</h1>

      <table class="table-preview">
        <tbody>
          <tr>
            <th>Defoult</th>
            <td>
              <button class="btn-medium btn-primary">Jetzt entdecken</button>
            </td>
            <td>
              <button class="btn-medium btn-primary-light">
                Jetzt entdecken
              </button>
            </td>
            <td>
              <div class="icon-state">
                <icon-edit-tool-zoom-out class="icon-state" />
              </div>
            </td>
          </tr>
          <tr>
            <th>Hover</th>
            <td>
              <button class="btn-medium btn-primary btn-hover-effect">
                Jetzt entdecken
              </button>
            </td>
            <td>
              <button class="btn-medium btn-primary-light btn-hover-effect">
                Jetzt entdecken
              </button>
            </td>
            <td>
              <div class="icon-state">
                <icon-edit-tool-zoom-out
                  class="icon-state icon-state-hover-effect"
                />
              </div>
            </td>
          </tr>
          <tr>
            <th>Active</th>
            <td>
              <button class="btn-medium btn-primary btn-acive-effect">
                Jetzt entdecken
              </button>
            </td>
            <td>
              <button class="btn-medium btn-primary-light btn-acive-effect">
                Jetzt entdecken
              </button>
            </td>
            <td>
              <div class="icon-state">
                <icon-edit-tool-zoom-out
                  class="icon-state icon-state-active-effect"
                />
              </div>
            </td>
          </tr>
          <tr>
            <th>Disable</th>
            <td>
              <button class="btn-medium btn-primary disabled">
                Jetzt entdecken
              </button>
            </td>
            <td>
              <button class="btn-medium btn-primary-light disabled">
                Jetzt entdecken
              </button>
            </td>
            <td>
              <div class="icon-state">
                <icon-edit-tool-zoom-out
                  class="icon-state icon-state-disabled-effect"
                />
              </div>
            </td>
          </tr>
          <tr>
            <th>Focus</th>
            <td>
              <button class="btn-medium btn-primary btn-focus-visible-effect">
                Jetzt entdecken
              </button>
            </td>
            <td>
              <button
                class="btn-medium btn-primary-light btn-focus-visible-effect"
              >
                Jetzt entdecken
              </button>
            </td>
            <td>
              <div class="icon-state">
                <icon-edit-tool-zoom-out
                  class="icon-state icon-state-focus-visible-effect"
                />
              </div>
            </td>
          </tr>
        </tbody>
      </table>
    </section>

    <section class="checkbox_text">
      <h1>Checkbox & Text</h1>

      <table class="table-preview">
        <tbody>
          <tr>
            <th>Defoult</th>
            <td class="bg-primary-light">
              <div class="checkbox">
                <label for="defoult-type">
                  <div
                    class="checkbox-marker"
                    :class="{ selected: isCheckbox }"
                  />
                  <input
                    id="defoult-type"
                    v-model="isCheckbox"
                    type="checkbox"
                  />

                  Lorem ipsum dolor sit amet.
                </label>
              </div>
            </td>
            <td>
              <span class="text-state">Preise</span>
            </td>
          </tr>
          <tr>
            <th>Hover</th>
            <td class="bg-primary-light">
              <div class="checkbox checkbox-hover-effect">
                <label for="hover-type">
                  <div
                    class="checkbox-marker"
                    :class="{ selected: isCheckbox }"
                  />
                  <input id="hover-type" v-model="isCheckbox" type="checkbox" />

                  Lorem ipsum dolor sit amet.
                </label>
              </div>
            </td>
            <td>
              <span class="text-state text-state-hover-effect">Preise</span>
            </td>
          </tr>
          <tr>
            <th>Active</th>
            <td class="bg-primary-light">
              <div class="checkbox checkbox-active-effect">
                <label for="active-type">
                  <div
                    class="checkbox-marker"
                    :class="{ selected: isCheckbox }"
                  />
                  <input
                    id="active-type"
                    v-model="isCheckbox"
                    type="checkbox"
                  />

                  Lorem ipsum dolor sit amet.
                </label>
              </div>
            </td>
            <td>
              <span class="text-state text-state-active-effect">Preise</span>
            </td>
          </tr>
          <tr>
            <th>Disable</th>
            <td class="bg-primary-light">
              <div class="checkbox disabled">
                <label for="disabled-type">
                  <div
                    class="checkbox-marker"
                    :class="{ selected: isCheckbox }"
                  />
                  <input
                    id="disabled-type"
                    v-model="isCheckbox"
                    type="checkbox"
                  />

                  Lorem ipsum dolor sit amet.
                </label>
              </div>
            </td>
            <td>
              <span class="text-state text-state-disable-effect">Preise</span>
            </td>
          </tr>
          <tr>
            <th>Focus</th>
            <td class="bg-primary-light">
              <div class="checkbox checkbox-focus-effect">
                <label for="focus-type">
                  <div
                    class="checkbox-marker"
                    :class="{ selected: isCheckbox }"
                  />
                  <input id="focus-type" v-model="isCheckbox" type="checkbox" />

                  Lorem ipsum dolor sit amet.
                </label>
              </div>
            </td>
            <td>
              <span class="text-state text-state-focus-visible-effect"
                >Preise</span
              >
            </td>
          </tr>
          <tr>
            <th>Selected</th>
            <td class="bg-primary-light">
              <div class="checkbox">
                <label for="selected-type">
                  <div class="checkbox-marker selected" />
                  <input id="selected-type" :value="true" type="checkbox" />

                  Lorem ipsum dolor sit amet.
                </label>
              </div>
            </td>
            <td>
              <span class="text-state text-state-selected-effect">Preise</span>
            </td>
          </tr>
          <tr>
            <th>Error</th>
            <td class="bg-primary-light">
              <div class="checkbox checkbox-error">
                <label for="error-type">
                  <div
                    class="checkbox-marker"
                    :class="{ selected: isCheckbox }"
                  />
                  <input id="error-type" v-model="isCheckbox" type="checkbox" />

                  Lorem ipsum dolor sit amet.
                </label>
              </div>
            </td>
            <td>
              <span class="text-state text-danger">Preise</span>
            </td>
          </tr>
        </tbody>
      </table>
    </section>

    <section class="input">
      <h1>Input</h1>

      <table class="table-preview">
        <tbody>
          <tr>
            <th>Defoult</th>
            <td class="bg-primary-light">
              <div
                class="form-field required"
                :class="{ 'field-error': exampleInput.isError }"
              >
                <label>Vorname</label>
                <input
                  v-model="exampleInput.value"
                  type="text"
                  :placeholder="exampleInput.placeholder"
                  required
                  @input="validateExampleInput"
                />
                <div class="error">{{ exampleInput.textError }}</div>
              </div>
            </td>
          </tr>
          <tr>
            <th>Disable</th>
            <td class="bg-primary-light">
              <div
                class="form-field required disabled"
                :class="{ 'field-error': exampleInput.isError }"
              >
                <label>Vorname</label>
                <input
                  v-model="exampleInput.value"
                  type="text"
                  :placeholder="exampleInput.placeholder"
                  required
                  @input="validateExampleInput"
                />
                <div class="error">{{ exampleInput.textError }}</div>
              </div>
            </td>
          </tr>
          <tr>
            <th>Error</th>
            <td class="bg-primary-light">
              <div class="form-field required field-error">
                <label>Vorname</label>
                <input
                  v-model="exampleInput.value"
                  type="text"
                  :placeholder="exampleInput.placeholder"
                  required
                  @input="validateExampleInput"
                />
                <div class="error">{{ exampleInput.textError }}</div>
              </div>
            </td>
          </tr>
        </tbody>
      </table>
    </section>
  </div>
</template>

<script>
import IconEditToolZoomOut from '@images/tabs/edit-tool-zoom-out.vue'

export default {
  name: 'Example',

  components: {
    IconEditToolZoomOut,
  },

  data: () => ({
    isCheckbox: false,

    exampleInput: {
      value: '',
      placeholder: 'Vorname placeholder',
      textError: 'Error text',
      isError: false,
    },
  }),

  methods: {
    validateExampleInput() {
      this.exampleInput.isError = !this.exampleInput.value.length
    },
  },
}
</script>

<style lang="scss">
.example {
  .typography,
  .colors {
    text-align: center;
  }

  h1 {
    margin: 10vw 0 4vw;
    font-size: 88px;
    opacity: 0.1;
    text-align: center;
  }

  .gap-24 {
    gap: 24px;
  }

  .color-box {
    margin-bottom: 32px;
    min-width: 120px;
    max-width: max-content;
    color: var(--dark);
    font-size: 20px;
    font-weight: 500;
    line-height: 1.3;
    text-align: center;

    .preview {
      margin-bottom: 28px;
      display: inline-block;
      width: 80px;
      height: 80px;
      border: 1px solid gray;
      border-radius: 50%;
    }

    .name {
      margin-bottom: 12px;
      opacity: 0.4;
    }
  }

  .table-preview {
    margin: 0 auto;

    th,
    td {
      padding: 8px;
    }

    th {
      font-size: 27px;
      font-weight: 400;
      text-align: left;
    }

    td {
      padding-right: 80px;
      padding-left: 80px;
    }
  }

  .bg-primary-light {
    background-color: var(--primary-light);
  }

  .input {
    .table-preview {
      width: 600px;

      td {
        padding-right: 24px;
        padding-left: 24px;
      }
    }
  }
}
</style>
